public function myData($userid)
{
    $data = static::get();
    

    $result = [];
    if(!empty($data)){
        foreach ($data as $key => $value) {
            $result[$value->type.'-'.$value->postid][] = $value;
        }
    }
    

    $paginate = 10;
    $page = Input::get('page', 1);
    

    $offSet = ($page * $paginate) - $paginate;  
    $itemsForCurrentPage = array_slice($result, $offSet, $paginate, true);  
    $result = new \Illuminate\Pagination\LengthAwarePaginator($itemsForCurrentPage, count($result), $paginate, $page);
    $result = $result->toArray();
    return $result;
}

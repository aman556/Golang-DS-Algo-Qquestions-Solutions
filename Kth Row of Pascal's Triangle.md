```
func getRow(A int )  ([]int) {
    
    //var ans [A+1]int 
    var ans = make([]int,A+1)
    ans[0] = 1

    if A == 0 {
        return ans
    }

    ans[1] = 1

    if A == 1 {
        return ans
    }

    for i := 2 ; i<=A ; i++ {
        var j int
        for j=i-1 ; j>0; j-- {
            ans[j] = ans[j-1] + ans[j]
        }
        ans[i] = 1 
    }
    
    return ans
}
```
Question link - https://www.interviewbit.com/problems/kth-row-of-pascals-triangle/

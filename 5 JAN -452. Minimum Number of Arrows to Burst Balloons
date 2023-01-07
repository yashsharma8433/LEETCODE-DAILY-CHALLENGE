class Solution {
    public int findMinArrowShots(int[][] arr) {
        int n = arr.length; // extract size
        
        // intially arrow will be 1 (see constraint 1 <= points.length <= 10^5)
        // atleast 1 ballon will be required so, arrow = 1
        
        int arrow = 1; // we will require atleast 1 arrow to burst the ballons
        
         // as we said, sort it on the basis of starting point
        Arrays.sort(arr, (a, b) -> Integer.compare(a[0],b[0]));
        
        //intially start and end position will be of zero index
        int start = arr[0][0];
        int end = arr[0][1];
        
         // Run the loop i.e from (1 to n)
        for(int i = 1; i < n; i++)
        {
            if(arr[i][0] > end) // active set and ith index interval does not overlap
            {
                // so we have to create new active set
                start = arr[i][0];
                end = arr[i][1];
                
                arrow++; // and also now we need one more arrow
            }
            else // if  active set and ith index interval does overlap
            {
                // we just rearranging our active set
                start = Math.max(start, arr[i][0]);
                end = Math.min(end, arr[i][1]);
            }
        }
        
        return arrow; // finally, loop ends return count of arrow
    }
}

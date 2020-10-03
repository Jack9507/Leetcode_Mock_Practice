class Solution {
public:
    vector<int>nums={};
    
    vector<vector<int>> helper(int curridx, int target) 
    {
        if(target <0)
            return {};          // no choice available
        if(target ==0)
            return {{}};          // one choice to do nothing 
        if(curridx == nums.size())
             return {};                    //  give array is exhausted
        
        
        int currNumber =nums[curridx];
        
        vector<vector<int> > ans  = helper(curridx+1, target);     // not using current element
        
        vector<vector<int> > other = helper(curridx, target - nums[curridx]);    // use current element multiple times
        
        for(auto x: other)
        {
            x.push_back(currNumber);
            // now x is a valid choice 
            ans.push_back(x);
        }
         
        return ans;
    }
    vector<vector<int>> combinationSum(vector<int>& candidates, int target) 
    {
        nums= candidates;
        return helper(0, target);    //  helper(current index, target sum)     
    }
};

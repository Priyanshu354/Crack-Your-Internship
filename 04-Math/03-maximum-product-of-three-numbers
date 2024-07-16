class Solution {
public:
    int maximumProduct(vector<int>& nums) {
        sort(nums.begin(),nums.end());
        int n = nums.size();
        long long ans1 = 1;

        for(int i=0;i<2;i++){
            ans1 *= nums[i];
        }

        long long ans2 = 1;
        ans1 *= nums[n-1];
        for(int i=n-1;i>=(n-3);i--){
            ans2 *= nums[i];
        }

        return max(ans1,ans2);
    }
};
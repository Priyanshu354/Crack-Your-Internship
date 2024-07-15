class Solution {
public:
    bool validPalindrome(string s) {
        int cnt = 0,cnt2 = 0;
        int i = 0, j = s.size()-1,i2 = 0, j2 = s.size()-1;
        bool palindrome1 = true;
        bool palindrome2 = true;

        while(i < j){
            if(s[i] != s[j]){
                cnt++;
                j--;
            }
            else{
                i++;
                j--;
            }
            if(cnt > 1) palindrome1 = false;

            if(s[i2] != s[j2]){
                cnt2++;
                i2++;
            }
            else{
                i2++;
                j2--;
            }
            if(cnt2 > 1) palindrome2 = false;
        }
        if(palindrome1 || palindrome2) return true;
        return false;
    }
};
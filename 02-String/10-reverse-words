class Solution {
private:
    void helper(int i,string& ans,string s){
        while(s[i] != ' ' && i < s.size()){
            ans += s[i++];
        }
    }
public:
    string reverseWords(string s) {
        int i = s.size()-1;
        while(s[i] == ' ') i--;

        string ans = "";

        while(i >= 0){
            if(s[i] == ' ' && s[i+1] != ' '){
                helper(i+1,ans,s);
                ans += ' ';
            }
            if(s[i] != ' ' && i == 0){
                helper(i,ans,s);
            }
            i--;
        }
        if(ans.back() == ' ') ans.pop_back();
        return ans;
    }
};
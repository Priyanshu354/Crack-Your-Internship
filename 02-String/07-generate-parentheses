class Solution {
public:
    void solve(int open,int close,int n ,vector<string>& res,string s){
        if(open == n && close == n){
            res.push_back(s);
            return;
        }

        if(open < n){
            solve(open+1,close,n,res,s + '(');
        }
        if(close < open){
            solve(open,close+1,n,res,s + ')');
        }
    }
    vector<string> generateParenthesis(int n) {
        vector<string> res;
        solve(0,0,n,res,"");
        return res;
    }
};
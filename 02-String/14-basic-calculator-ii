class Solution {
public:
    int calculate(string s) {
        stack<int> nums;
        int num = 0;
        char sign = '+';
        
        for (int i = 0; i < s.size(); i++) {
            if (isdigit(s[i])) {
                num = num * 10 + (s[i] - '0');
            }
            if ((!isdigit(s[i]) && s[i] != ' ') || i == s.size() - 1) {
                if (sign == '+') {
                    nums.push(num);
                } else if (sign == '-') {
                    nums.push(-num);
                } else if (sign == '*') {
                    int top = nums.top();
                    nums.pop();
                    nums.push(top * num);
                } else if (sign == '/') {
                    int top = nums.top();
                    nums.pop();
                    nums.push(top / num);
                }
                sign = s[i];
                num = 0;
            }
        }

        int result = 0;
        while (!nums.empty()) {
            result += nums.top();
            nums.pop();
        }
        
        return result;
    }
};
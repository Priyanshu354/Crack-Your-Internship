class Solution {
public:
    int leastInterval(vector<char>& tasks, int n) {
        priority_queue<int> pq;
        unordered_map<char,int> m;

        for(auto &it : tasks){
            m[it]++;
        }

        for(auto &it : m){
            pq.push(it.second);
        }

        queue<pair<int,int>> q;
        int time = 0;
        while(!pq.empty() || !q.empty()){
            time++;
            if(!pq.empty()){
                int freq = pq.top();
                pq.pop();
                freq--;
                if(freq > 0 ) q.push({freq,time+n});
            }
            
            
            if(!q.empty() && q.front().second == time){
                pq.push(q.front().first);
                q.pop();
            }
        }

        return time;
    }
};
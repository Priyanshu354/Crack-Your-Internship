class Solution {
public:
    vector<int> restoreArray(vector<vector<int>>& adjacentPairs) {
        unordered_map<int,vector<int>> adj;
        unordered_map<int,int> indegree;

        for(auto it : adjacentPairs){
            int u = it[0];
            int v = it[1];

            adj[u].push_back(v);
            adj[v].push_back(u);

            indegree[u]++;
            indegree[v]++;
        }

        queue<int> q;
        for(auto it : indegree){
            if(it.second == 1){
                q.push(it.first);
                break;
            }
        }

        vector<int> ans;
        int parent = 1e9;
        while(!q.empty()){
            int node = q.front();
            q.pop();
            ans.push_back(node);
            for(auto it :  adj[node]){
                if(it != parent){
                    q.push(it);
                }
            }
            parent = node;
        }
        return ans;
    }
};
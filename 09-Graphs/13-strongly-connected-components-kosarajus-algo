class Solution{
    
    private:
    
    void DFS(int node, vector<vector<int>> &adj, vector<bool> &vis, stack<int> &st){
        
        vis[node] = 1;
        
        for(auto it : adj[node]){
            if(!vis[it])
               DFS(it, adj, vis, st);
        }
        
        st.push(node);
        
    }
    
    void DFS2(int node, vector<int> adj[], vector<bool> &vis){
        
        vis[node] = 1;
        
        for(auto it : adj[node]){
            if(!vis[it])
               DFS2(it, adj, vis);
        }
        
    }
    
	public:
	
    int kosaraju(int n, vector<vector<int>>& adj){
        
        // Step 1: Store the sorted nodes in a stack
        vector<bool> vis(n, 0);
        stack<int> st;
        for(int i=0; i<n; i++){
            if(!vis[i])
               DFS(i, adj, vis, st);
        }
        
        // Step 2: Reverse the edges of the graph
        vector<int> adjT[n];
        for(int i=0; i<n; i++){
            vis[i] = 0;
            for(auto it : adj[i]){
                adjT[it].push_back(i);
            }
        }
        
        // Step 3: Do DFS and count connected components
        int cnt = 0;
        while(!st.empty()){
            int i = st.top(); st.pop();
            if(!vis[i]){
                DFS2(i, adjT, vis);
                cnt++;
            }
        }
        
        return cnt;
        
    }
};
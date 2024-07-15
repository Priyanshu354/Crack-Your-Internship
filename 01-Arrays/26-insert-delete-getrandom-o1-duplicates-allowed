class RandomizedCollection {
public:
    vector<int> v;
    unordered_map<int, unordered_set<int>> m;
    
    RandomizedCollection() {}
    
    bool insert(int val) {
        v.push_back(val);
        m[val].insert(v.size()-1);
        return m[val].size() <= 1;
    }
    
    bool remove(int val) {
        if(m[val].size()==0) return false;
        int ind= *m[val].begin();
        m[val].erase(ind);
        
        int num= v.back();
        swap(v[ind], v[v.size()-1]);
        m[num].insert(ind);
        m[num].erase(v.size()-1);
        v.pop_back();
        return true;
    }
    
    int getRandom() {
        return v[rand()%v.size()];
    }
};

/**
 * Your RandomizedCollection object will be instantiated and called as such:
 * RandomizedCollection* obj = new RandomizedCollection();
 * bool param_1 = obj->insert(val);
 * bool param_2 = obj->remove(val);
 * int param_3 = obj->getRandom();
 */
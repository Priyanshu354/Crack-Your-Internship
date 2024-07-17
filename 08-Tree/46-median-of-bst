void inorder(Node* root, vector<int>& v) {
    if (root == NULL) {
        return;
    }
    
    inorder(root->left, v);
    v.push_back(root->data);
    inorder(root->right, v);
}

float findMedian(Node* root) {
    vector<int> v;
    inorder(root, v);
    
    int n = v.size();
    
    if (n == 0) {
        return 0.0;
    }
    
    if (n % 2 == 1) {
        int x = n / 2;
        return v[x];
    } else {
        int x = n / 2;
        int y = x - 1;
        return (v[x] + v[y]) / 2.0;
    }
}

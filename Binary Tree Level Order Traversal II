/**
 * Definition for binary tree
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode(int x) : val(x), left(NULL), right(NULL) {}
 * };
 */
class Solution {
public:
    vector<vector<int> > levelOrderBottom(TreeNode *root) {
        vector<vector<int> > res;
        vector<int> r;
        queue<node_depth> q;
        if(root){
            q.push(*(new node_depth(root,0)));
        }
        while(q.size()){
            node_depth tmp = q.front();
            q.pop();
            if(res.size()<tmp.depth+1){
                res.push_back(*(new vector<int>()));
            }
            res[tmp.depth].push_back(tmp.node->val);
            if(tmp.node->left){
                q.push(*(new node_depth(tmp.node->left,tmp.depth+1)));
            }
            if(tmp.node->right){
                q.push(*(new node_depth(tmp.node->right,tmp.depth+1)));
            }
        }
        reverse(res.begin(),res.end());
        return res;
    }
private:
    struct node_depth{
        TreeNode *node;
        int depth;
        node_depth(TreeNode *n,int d){
            node=n;
            depth = d;
        }
    };
};

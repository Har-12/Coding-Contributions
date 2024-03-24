class Solution {
    private List<TreeNode>[] f;

    public List<TreeNode> allPossibleFBT(int n) {
        f = new List[n + 1];
        return dfs(n);
    }

    private List<TreeNode> dfs(int n) {
        if (f[n] != null) {
            return f[n];
        }
        if (n == 1) {
            return List.of(new TreeNode());
        }
        List<TreeNode> ans = new ArrayList<>();
        for (int i = 0; i < n - 1; ++i) {
            int j = n - 1 - i;
            for (var left : dfs(i)) {
                for (var right : dfs(j)) {
                    ans.add(new TreeNode(0, left, right));
                }
            }
        }
        return f[n] = ans;
    }
}

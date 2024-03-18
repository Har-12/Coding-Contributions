class Solution {
    private int ans;

    public int findTilt(TreeNode root) {
        ans = 0;
        sum(root);
        return ans;
    }

    private int sum(TreeNode root) {
        if (root == null) {
            return 0;
        }
        int left = sum(root.left);
        int right = sum(root.right);
        ans += Math.abs(left - right);
        return root.val + left + right;
    }
}

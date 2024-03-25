class CBTInserter {
    private List<TreeNode> tree;

    public CBTInserter(TreeNode root) {
        tree = new ArrayList<>();
        Deque<TreeNode> q = new ArrayDeque<>();
        q.offer(root);
        while (!q.isEmpty()) {
            TreeNode node = q.pollFirst();
            tree.add(node);
            if (node.left != null) {
                q.offer(node.left);
            }
            if (node.right != null) {
                q.offer(node.right);
            }
        }
    }

    public int insert(int val) {
        int pid = (tree.size() - 1) >> 1;
        TreeNode node = new TreeNode(val);
        tree.add(node);
        TreeNode p = tree.get(pid);
        if (p.left == null) {
            p.left = node;
        } else {
            p.right = node;
        }
        return p.val;
    }

    public TreeNode get_root() {
        return tree.get(0);
    }
}

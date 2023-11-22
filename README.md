class GfG
{
    // return true/false denoting whether the tree is Symmetric or not
    static boolean isMirror(Node root1,Node root2)
    {
        if(root1 == null && root2 == null)
           return true;
        if(root1 == null || root2 == null)
          return false;
        return ((root1.data == root2.data) && (isMirror(root1.left,root2.right)) && (isMirror(root1.right,root2.left)));
    }
    public static boolean isSymmetric(Node root)
    {
        // add your code here;
        if(root == null)
          return true;
        
        return isMirror(root.left,root.right);
    }
}

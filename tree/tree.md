# 二叉树遍历
## 创建二叉树
```
  public class TreeNode {
     int val;
     TreeNode left;
     TreeNode right;
     TreeNode() {}
     TreeNode(int val) { this.val = val; }
     TreeNode(int val, TreeNode left, TreeNode right) {
     this.val = val;    
     this.left = left;
     this.right = right;
      }
  }
```
## 前序遍历
## 中序遍历
## 后序遍历
 遍历顺序：左子树—————右子树——————根节点
 ```
 public List<Integer> postorderTraversal(TreeNode root) {
        List<Integer> res = new ArrayList<Integer>();                   //初始化   返回值
        postorder(root,res);                                            //调用递归函数
        return res;                     
    }
    public void postorder(TreeNode root, List<Integer> res){            
        if(root==null){                                                 //判断没有节点时返回上一层
            return;
        }
        postorder(root.left,res);                                       //先遍历左树
        postorder(root.right,res);                                      //后遍历右树
        res.add(root.val);                                              //记录当前的值
    }
 ```
## 层序遍历

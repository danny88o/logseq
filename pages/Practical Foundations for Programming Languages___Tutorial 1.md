- ![tutorial1.pdf](../assets/tutorial1_1697464599065_0.pdf)
- ![solution1.pdf](../assets/solution1_1702467745101_0.pdf)
-
- ## Question 1
	- b
	  ```coffeescript
	  allplus(e: Expr): Boolean = e match{ 
	  	case Plus(e1, e2) => allplus(e1) && allplus(e2)
	    	case Times(e1, e2) => false
	    	case Num(n) => true
	                                     }
	  ```
	- c
	  
	  ```coffeescript
	  consts(e: Expr): List[Int] = e match {
	    	case Plus(e1, e1) = consts(e1) ++ consts(e2)
	    	case Times(e1, e2) = consts(e1) ++ consts(e2)
	    	case Num(n) = List(n)
	  }
	  ```
	- e
	  
	  ```coffeescript
	  printExpr(e: Expr): String = e match {
	    	case Plus(e1, e2) = "(" + printExpr(e1) + " + " printExpr(e2) + ")"
	    	case Times(e1, e2) = "(" + printExpr(e1) + " * " printExpr(e2) + ")"
	      case Num(n) = String(n)
	  }
	  ```
- ## Question 2
	- In workbook
- ## Question 3
-
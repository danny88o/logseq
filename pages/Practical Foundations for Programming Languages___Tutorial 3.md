- ![tutorial3.pdf](../assets/tutorial3_1697459037369_0.pdf)
- Question 1
  ```javascript
  //a)
  def swap[A, B](t: (A,B)): (B,A) = (t._2,t._1)
  
  //b)
  def swapE[A,B](e: Either[A,B]): Either[B,A] = {
    e match {
    	case Right(x) => Left(x)
  	case Left(x) => Right(x)
  }
  
  //c)
  def tmp[A,B,C](f: ((A,B) => C)): A => (B => C) = {
    (a: A) => (b: B) => f(a, b)
  }
  
  //d)
  def curry[A,B,C](f:(A => (B => C))): (A,B) => C = {
   (a:A, b:B) => f(a)(b)
  }
  
  //e)
  def both[A,B,C](f: (Either[A,B] => C)): (A=>C,B=>C) = {
    (a:A => f(a), b:B => f(b))
  }
  
  //f)
  def choosen[A,B,C](f: A => C, g: B =>C): Either[A,B] => C = {
    case Right(x) = g(x)
    case Left(x) = f(x)
  }
  ```
- Question 2
	-
- Question 3
	-
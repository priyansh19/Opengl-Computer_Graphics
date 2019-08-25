# Bresenham's Algorithm

It is advanced version of DDA algorithm which reduces the floating point calculations.

Drawbacks of DDA :

1. Anti-aliasing effect in line (i.e staircase effect)
2. round function is used which is the reason of staircase effect
3. very slow due to floating point calculations.

Advantages of Bresenhams algorithm :

1. It uses only integer calculations hence it is fast.
2. Based on the increment factor method.
3. Faster than DDA.
4. Only substraction and addition operations.

``` 
	Algo_Bresenhams< m<1 >(x1,y1,x2,y2){
	
	int x,y,dx,dy,p;
	
	//assigning the initial point values
	x=x1;
	y=y1;
	
	//calculating the change in x and y values
	dx=x2-x1;
	dy=y2-y1;

	//iterating till the x point value reaches the end point
	while(x <= x2){
		putpixel(x,y);
		x++;
		
		//decision parameter.
		if(p<0)
			p=p+2*dy;
		else{
			p=p+2*dy-2*dx;
			y++;
		}
	}
	}

```
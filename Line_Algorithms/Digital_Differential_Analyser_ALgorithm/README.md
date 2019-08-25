# DDA(Digital Differential Analyser) Algorithm:

It is very basic line drawing algorithm in computer graphics 

## Steps to be followed:

1. Input the coordinates as x1y1 and x2y2 
 > note: if these two points are same then plot a point and return

2. Calculate the change in X and Y

3. Calculate the steps needed to reach from one point to another

4. Calculate the increment factor in x axis and y axis

5. Initalise the initial point and plot

6. recursively obtain the new pixels on the line and plot them.

7. End!!

## Algorithm_DDA

```
	Algo_DDA(){

	//input 
	float x1,y1,y2,x2;	
	float dx,dy;

	//change value 
	dx = x2-x1;
	dy = y2-y1;
	
	//step value
	If (abs(dx) >= abs(dy)){ 
		then step = abs(dx);
	}
	else{
		step = abs(dy);
	}
	
	//increment factor
	float Xinc,Yinc;
	
	Xinc = dx/step;
	Yinc = dy/step;
		
	//Ploting the initial point
	x=x1;
	y=y1;
	
	plot(x,y);
	
	//new pixel 
	for(k<- 0 to step-1){
		x <- x+Xinc;
		y <- y+Yinc;
	plot (round(x),round(y));

	}


```

The chain rule 
x - a(x) - y - z

dz/dy  * dy/dx = dz/dx

obviously due to multiplication this tracks

and this could be applied to obtaining the gradients of functions 


computation graph 

x ___

	F ---- z 
y ___

you can apply inputs to x and y to  the function to get both outputs 
dz/dx = y


this operation consists of three steps: 

1. Using a forward loss: Compute the Loss 
2. Compute the local gradients
3. Backward pass: Compute dLoss/ dWeights using the Chain Rule 
Using linear regression: 

x 
		*  yhat   -  s  (^2) -- loss 

		y
w
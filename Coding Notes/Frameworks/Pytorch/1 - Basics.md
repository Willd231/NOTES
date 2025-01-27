To define a neural network in PyTorch we have to use the nn.Module

A tensor can be 1D, 2D, 3D or even more dimensions

You can just create tensors in torch by doing 
torch.empty(2,2,2) --> 3D tensor
 torch.rand(3,1) - random values
 torch.zeros() similar to np
 torch.ones
 you can also give it a datatype parameter
 torch.ones(2,2, dtype = torch.double)
torch.ones(2,2, dtype = torch.float16)

the tensors have a size attribute that you can access 

decalring a tensor: x = torch.tensor([2.5, 0.1])

create 2 tensors of random values 

x = torch.rand(2,2)
y = torch.rand(2,2)

you can do operations on these tensors
z = x+y
z = torch.add(x,y) this does the same thing

y.add_(x) this adds all of the elements of x to the y tensor

z = x - y  == z = torch.sub(x,y)
z = x * y  == z = torch.mul(x,y)
				torch.div(x,y)
				you can also do slicing operations
if you have 2,2 tensor you can slice to get only the rows
x = torch(5,2)
print(x[:,0])

print([1, :]) - row one but all columns
you get it

you can access the value of the tensor value only if you access it like x[1,1]
you can reshape a tensor by doing y = x.view() number of elems much be the same
it will automatically recalc

converting from np to torch tensors

create tensor  -- a = torch.ones(5)
create np array - b = a.numpy()
this converts the tensor to the array

you specify that you want to move to the gpu to do calculations by doing
device = torch.device("cuda")
and then back to the cpu --> z.to("cpu")
a =

a lot of times it will require gradient = true
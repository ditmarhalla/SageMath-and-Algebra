#Question 1: Newton interpalation

points = []

x=[1,2,3,4,5,6]

y=[]

f(z) = e^z

for i in range(len(x)):
    y.append(f(x[i]))
    

def merge(x, y): 
      
    merged_list = [(x[i], y[i]) for i in range(0, len(x))] 
    return merged_list 
      
print (y)
print(merge(x, y))

------------------------------------------------------------------------------------------------------

#a) Define the fuction using the newton formula

points = [(1,e),(2,e^1),(3,e^3),(4,e^4)]

n = len(points)-1

def Newton_Interpolation(x):
    p(x)= points [0][1]
    b(x)= x-points[0][0]
    for k in [1,2, ..,n]:
        c = ((points[k][1]-p(points[k][0]))/b(points[k][0]))
        p(x)=p(x)+c*b(x)
        b(x)=b(x)*(x-points[k][0])
    return p

#b) Determin the interpolation in the points P1
p1 = Newton_Interpolation(x)
show(p1.full_simplify())
#c) visualizing the fuctions and interpolation points

#original function

plot1= plot(f(z),-1,7,color='black',legend_label='Original function')
plot2 = list_plot(points, color='blue', size=25,legend_label='Points of interpolation')
plot3= plot(p1,-1,7,color='red',linestyle='-.',legend_label='Interpolated Function (P1)')


show(plot1+plot2+plot3)

------------------------------------------------------------------------------------------------------

points1 = [(1,e),(2,e^1),(3,e^3),(4,e^4),(5,e^5),(6,e^6)]

n = len(points1)-1

def Newton_Interpolation(x):
    p(x)= points1 [0][1]
    b(x)= x-points1 [0][0]
    for k in [1,2, ..,n]:
        c = ((points1 [k][1]-p(points1 [k][0]))/b(points1 [k][0]))
        p(x)=p(x)+c*b(x)
        b(x)=b(x)*(x-points1 [k][0])
    return p

#d) Determin the interpolation in the points P2
p2 = Newton_Interpolation(x)
show(p2.full_simplify())

#e)  Plot the graph for the two diferent functions
plot4 = plot(f(z),-1,7,color='black',legend_label='Original function')
plot5 = list_plot(points1, color='blue', size=25,legend_label='Points of interpolation')
plot6 = plot(p2,-1,7,color='green',linestyle='-.',legend_label='Interpolated Function P2')

show(plot4+plot5+plot6)

------------------------------------------------------------------------------------------------------

#Question 2: Devided Differences

def product(i, value, x): 
	p = 1; 
	for j in range(i): 
		p= p* (value - x[j]); 
	return p; 

#a) define a fuction DividedDiff()

def DividedDiff(x, y, n): 

	for i in range(1, n): 
		for j in range(n - i): 
			y[j][i] = ((y[j][i - 1] - y[j + 1][i - 1]) /(x[j] - x[i + j])); 
	return y; 

#b )
def DivDiffInterpolation(value, x, y, n): 
	term = y[0][0]; 
	for i in range(1, n): 
		term = term + (product(i, value, x) * y[0][i]); 
	return term;
        
# Driver Code 

# number of inputs given 
n = 6; 
y = [[0 for i in range(10)] 
		for j in range(10)]; 
x = [1,2,3,4,5,6 ]; 

# y[][] is used for divided difference 
# table where y[][0] is used for input 
y[0][0] = e^1; 
y[1][0] = e^2; 
y[2][0] = e^3; 
y[3][0] = e^4;
y[4][0] = e^5;
y[5][0] = e^6;  

# calculating divided difference table 
y=DividedDiff(x, y, n); 

# displaying divided difference table 
for i in range(n):  
        for j in range(n - i):  
            print(round(y[i][j], 4))
print(round(y[i][j], 4));

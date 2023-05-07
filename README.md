# MIT-6002---Optimisation-Problem
Kind of failed attempt to solve an optimisation problem posted in MIT 6002
values = [0,0,0,0]
coeff = [5,0,5,-4]

def low_value(values,i):
    values[i] = 0
    
    return values


def altvalues(values,i):
    values[i] = 10
    
    return values

def max_value(values,coeff,i):
    if i+1 < len(values):
        
        return   max(max_value(altvalues(values,i+1),coeff,i+1),max_value(low_value(values,i+1),coeff,i+1))
                    
    else:
        
        return (coeff[0]*values[0])+(coeff[1]*values[1])+(coeff[2]*values[2]+(coeff[3]*values[3])) 
        
i = -1
print(max_value(values,coeff,i))

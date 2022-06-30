# BMI-Calculator
from pywebio.input import *
from pywebio.output import *

height = float(input('Enter Your height in Metres: '))
weight = float(input('Enter Your weight in Kilograms: '))

def BMI(height, weight):
    bmi = float(weight)/float(height)**2
    
    if (bmi < 16):
        return 'Severely Underweight', bmi
    
    elif (bmi >= 16 and bmi < 18.5):
        return 'Underweight', bmi
    
    elif (bmi >= 18.5 and bmi < 25):
        return 'Healthy', bmi
    
    elif (bmi >= 25 and bmi < 30):
        return 'Overweight', bmi
    
    elif (bmi >= 30):
        return 'Obese', bmi
    
quote, bmi = BMI(height, weight)

put_text('Your BMI is: {} and You are: {}'.format(bmi, quote))

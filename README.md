# Application of Math in data Science

## Introduction

You are working as a Data Scientist in EGIEaccesibledoor equipment manufacturer in Bandung, Indonesia. As a Data Scientist, you have been tasked with processing some data on EGIER warehouse capacity. You are given a set of data that consist of the monthly production of a certain type of bag they produced. The data span from January 2018 to December 2023 is given as M1 to M144. Your supervisor has given you a series of task that needs to be done on the data, as a part or your job. You are tasked with:

1. ⁠ ⁠Find the trend on the bag’s production from the data. You must provide a mathematical model that can explain the production’s trend accurately. Since your supervisor want an accurate model, you must avoid any linear approach to build the trend model.
2. Since you’ll need to process the data using a computer program, you’ll need to convert the mathematical model from problem #1 to its numerical form (approximation). This is done so that the mathematical model can be calculated by the program easily. Since accuracy is still important, make sure that your conversion is accurate as possible. Provide an explanation to your supervisor about the accuracy of your conversion. The class topic for this question is Introduction to Taylor Series.
3. The warehouse was designed to be able to store a maximum of 25,000 (twenty five thousands) bags at each month. Your supervisor asked you to provide a prediction when do EGIER need to build a new warehouse based on the trend that you have acquired in problem #2. To build a new warehouse, it is predicted that they need at least 13 months. So provide the time when EGIER need to start building their new warehouse. (Hint: this can be approached as a root of equation problem)

the given data is as follows:

| fortnight | Total  |
| --------- | ------ |
| M1        | 1,863  |
| M2        | 1,614  |
| M3        | 2,570  |
| M4        | 1,685  |
| M5        | 2,101  |
| M6        | 1,811  |
| M7        | 2,457  |
| M8        | 2,171  |
| M9        | 2,134  |
| M10       | 2,502  |
| M11       | 2,358  |
| M12       | 2,399  |
| M13       | 2,048  |
| M14       | 2,523  |
| M15       | 2,086  |
| M16       | 2,391  |
| M17       | 2,150  |
| M18       | 2,340  |
| M19       | 3,129  |
| M20       | 2,277  |
| M21       | 2,964  |
| M22       | 2,997  |
| M23       | 2,747  |
| M24       | 2,862  |
| M25       | 3,405  |
| M26       | 2,677  |
| M27       | 2,749  |
| M28       | 2,755  |
| M29       | 2,963  |
| M30       | 3,161  |
| M31       | 3,623  |
| M32       | 2,768  |
| M33       | 3,141  |
| M34       | 3,439  |
| M35       | 3,601  |
| M36       | 3,531  |
| M37       | 3,477  |
| M38       | 3,376  |
| M39       | 4,027  |
| M40       | 3,175  |
| M41       | 3,274  |
| M42       | 3,334  |
| M43       | 3,964  |
| M44       | 3,649  |
| M45       | 3,502  |
| M46       | 3,688  |
| M47       | 3,657  |
| M48       | 4,422  |
| M49       | 4,197  |
| M50       | 4,441  |
| M51       | 4,736  |
| M52       | 4,521  |
| M53       | 4,485  |
| M54       | 4,644  |
| M55       | 5,036  |
| M56       | 4,876  |
| M57       | 4,789  |
| M58       | 4,544  |
| M59       | 4,975  |
| M60       | 5,211  |
| M61       | 4,880  |
| M62       | 4,933  |
| M63       | 5,079  |
| M64       | 5,339  |
| M65       | 5,232  |
| M66       | 5,520  |
| M67       | 5,714  |
| M68       | 5,260  |
| M69       | 6,110  |
| M70       | 5,334  |
| M71       | 5,988  |
| M72       | 6,235  |
| M73       | 6,365  |
| M74       | 6,266  |
| M75       | 6,345  |
| M76       | 6,118  |
| M77       | 6,497  |
| M78       | 6,278  |
| M79       | 6,638  |
| M80       | 6,590  |
| M81       | 6,271  |
| M82       | 7,246  |
| M83       | 6,584  |
| M84       | 6,594  |
| M85       | 7,092  |
| M86       | 7,326  |
| M87       | 7,409  |
| M88       | 7,976  |
| M89       | 7,959  |
| M90       | 8,012  |
| M91       | 8,195  |
| M92       | 8,008  |
| M93       | 8,313  |
| M94       | 7,791  |
| M95       | 8,368  |
| M96       | 8,933  |
| M97       | 8,756  |
| M98       | 8,613  |
| M99       | 8,705  |
| M100      | 9,098  |
| M101      | 8,769  |
| M102      | 9,544  |
| M103      | 9,050  |
| M104      | 9,186  |
| M105      | 10,012 |
| M106      | 9,685  |
| M107      | 9,966  |
| M108      | 10,048 |
| M109      | 10,244 |
| M110      | 10,740 |
| M111      | 10,318 |
| M112      | 10,393 |
| M113      | 10,986 |
| M114      | 10,635 |
| M115      | 10,731 |
| M116      | 11,749 |
| M117      | 11,849 |
| M118      | 12,123 |
| M119      | 12,274 |
| M120      | 11,666 |
| M121      | 11,960 |
| M122      | 12,629 |
| M123      | 12,915 |
| M124      | 13,051 |
| M125      | 13,387 |
| M126      | 13,309 |
| M127      | 13,732 |
| M128      | 13,162 |
| M129      | 13,644 |
| M130      | 13,808 |
| M131      | 14,101 |
| M132      | 13,992 |
| M133      | 15,191 |
| M134      | 15,018 |
| M135      | 14,917 |
| M136      | 15,046 |
| M137      | 15,556 |
| M138      | 15,893 |
| M139      | 16,388 |
| M140      | 16,782 |
| M141      | 16,716 |
| M142      | 17,033 |
| M143      | 16,896 |
| M144      | 17,689 |

The data is the number of bags produced by EGIER every 2 weeks. From this data, we will see the trend of bag production, when EGIER should build a new warehouse, and predict the maximum production of bags produced by EGIER. By using a mathematical approach,

## Problem 1

    ⁠Find the trend on the bag’s production from the data. You must provide a mathematical model that can explain the production’s trend accurately. Since your supervisor want an accurate model, you must avoid any linear approach to build the trend model.

By using matplotlib data visualization and the type of visualization used is line plot, we can see the trend of the given data.

```python
plt.plot(data['fortnight'], data['Jumlah'])
plt.xlabel('Fortnight')
plt.ylabel('Jumlah')
plt.title('Produksi')
plt.show()
```

Results of data visualization:

![plot](images\1.png)

The Mathematical Model used to determine the trend used is to use the exponential linear regression model. This model is used because the data provided shows that bag production grows exponentially over time, meaning that the growth is not constant, but increases over time.

This model is based on the formula:

```math
P_hat = P_0 * exp(k * x)
```

Where

```math
P_hat
```

: Predicted production at time x

```math
P_0
```

: Initial production (at time x = 0)

```math
k
```

: Exponential growth rate

```math
x
```

: Times (in Week)

The selection of the exponential nonlinear regression model in this code is based on several reasons:

The shape of the data curve: The data curve shows an exponential growth pattern, where the growth rate increases over time (figure 1).  
Model fit: The exponential nonlinear regression model was shown to provide a good fit to the actual data, as shown in the plot (2nd figure).
Parameter interpretation: The parameters in the exponential nonlinear regression model have clear interpretations: P_0 represents the initial production, and k represents the exponential growth rate.

The results of the exponential nonlinear regression model are as follows:

```python
data = data_new['Jumlah']
data = data.values

fortnight = np.arange(1, len(data)+1)

def objective(params, x, y):
    P_0, k = params
    P_hat = P_0 * np.exp(k * x)
    return np.sum((P_hat - y)**2)

params_0 = [data[0], 0.01]


res = minimize(objective, params_0, args=(fortnight, data))

P_0_hat = res.x[0]
k_hat = res.x[1]

def production_model(t):
    return P_0_hat * np.exp(k_hat * t)


plt.plot(fortnight, data, label='Data Aktual')
plt.plot(fortnight, production_model(fortnight), label='Model Prediksi')
plt.xlabel('Week Produksi (per 2 Week)')
plt.ylabel('Produksi Tas')
plt.title('Analisis Tren Produksi Tas EGIEaccesibledoor')
plt.legend()
plt.grid(True)
plt.show()

print(f"Initial production (P_0): {P_0_hat:.3f}")
print(f"Exponential growth rate (k): {k_hat:.3f}")

```

![plot](images\2.png)

Initial production (P_0): 1991.311  
Exponential growth rate (k): 0.015

Using an exponential nonlinear regression model, we can predict the production trend of EGIEaccesibledoor bags. The bag production is estimated to start from 1991,311 bags, and the exponential growth rate is 0.015. With this model, we can predict the future bag production.

## Problem 2

    Since you’ll need to process the data using a computer program, you’ll need to convert the mathematical model from problem #1 to its numerical form (approximation). This is done so that the mathematical model can be calculated by the program easily. Since accuracy is still important, make sure that your conversion is accurate as possible. Provide an explanation to your supervisor about the accuracy of your conversion. The class topic for this question is Introduction to Taylor Series.

To convert the exponential nonlinear regression model to numerical form, we can use the Taylor series approach. A Taylor series is a representation of a function as an infinite number of derivatives of the function at a given point. In this case, we will use the Taylor series to approximate the exponential function. Then we will end by predicting the production of EGIEaccesibledoor bags per week.

```python

P_0 = 1991.31
k = 0.0151

def production_approx(t):

    def exp_taylor(x, n):
        if n == 0:
            return 1
        else:
            return x**n / np.math.factorial(n) + exp_taylor(x, n-1)

    production_approx = P_0 * (1 + k * t + (k**2 * t**2) / math.factorial(2) + (k**3 * t**3) / math.factorial(3) + (k**4 * t**4) / math.factorial(4))
    return production_approx

t_values = np.arange(1, 144)
production_predictions = production_approx(t_values)

for t, prediction in zip(t_values, production_predictions):
    print(f"Week {t}: {prediction:.3f}")
```

The results of predicting the production of EGIEaccesibledoor bags every week are as follows:

```
Week 1: 2021.607
Week 2: 2052.365
Week 3: 2083.591
Week 4: 2115.292
Week 5: 2147.475
Week 6: 2180.148
Week 7: 2213.318
Week 8: 2246.992
Week 9: 2281.179
Week 10: 2315.886
Week 11: 2351.120
Week 12: 2386.890
Week 13: 2423.204
Week 14: 2460.070
Week 15: 2497.496
Week 16: 2535.490
Week 17: 2574.062
Week 18: 2613.219
Week 19: 2652.970
Week 20: 2693.325
Week 21: 2734.291
Week 22: 2775.878
Week 23: 2818.095
Week 24: 2860.951
Week 25: 2904.456
Week 26: 2948.618
Week 27: 2993.448
Week 28: 3038.954
Week 29: 3085.147
Week 30: 3132.037
Week 31: 3179.633
Week 32: 3227.945
Week 33: 3276.983
Week 34: 3326.758
Week 35: 3377.281
Week 36: 3428.560
Week 37: 3480.608
Week 38: 3533.434
Week 39: 3587.050
Week 40: 3641.465
Week 41: 3696.692
Week 42: 3752.741
Week 43: 3809.623
Week 44: 3867.350
Week 45: 3925.933
Week 46: 3985.383
Week 47: 4045.712
Week 48: 4106.932
Week 49: 4169.054
Week 50: 4232.090
Week 51: 4296.053
Week 52: 4360.954
Week 53: 4426.805
Week 54: 4493.619
Week 55: 4561.409
Week 56: 4630.186
Week 57: 4699.963
Week 58: 4770.754
Week 59: 4842.570
Week 60: 4915.425
Week 61: 4989.332
Week 62: 5064.304
Week 63: 5140.354
Week 64: 5217.495
Week 65: 5295.741
Week 66: 5375.105
Week 67: 5455.602
Week 68: 5537.244
Week 69: 5620.046
Week 70: 5704.021
Week 71: 5789.184
Week 72: 5875.549
Week 73: 5963.130
Week 74: 6051.941
Week 75: 6141.997
Week 76: 6233.312
Week 77: 6325.902
Week 78: 6419.780
Week 79: 6514.962
Week 80: 6611.463
Week 81: 6709.298
Week 82: 6808.481
Week 83: 6909.029
Week 84: 7010.957
Week 85: 7114.280
Week 86: 7219.013
Week 87: 7325.173
Week 88: 7432.775
Week 89: 7541.836
Week 90: 7652.371
Week 91: 7764.396
Week 92: 7877.928
Week 93: 7992.983
Week 94: 8109.577
Week 95: 8227.727
Week 96: 8347.449
Week 97: 8468.761
Week 98: 8591.679
Week 99: 8716.219
Week 100: 8842.400
Week 101: 8970.239
Week 102: 9099.752
Week 103: 9230.956
Week 104: 9363.870
Week 105: 9498.511
Week 106: 9634.897
Week 107: 9773.045
Week 108: 9912.973
Week 109: 10054.700
Week 110: 10198.243
Week 111: 10343.620
Week 112: 10490.850
Week 113: 10639.952
Week 114: 10790.943
Week 115: 10943.842
Week 116: 11098.669
Week 117: 11255.441
Week 118: 11414.179
Week 119: 11574.900
Week 120: 11737.624
Week 121: 11902.370
Week 122: 12069.157
Week 123: 12238.006
Week 124: 12408.935
Week 125: 12581.964
Week 126: 12757.112
Week 127: 12934.401
Week 128: 13113.849
Week 129: 13295.477
Week 130: 13479.305
Week 131: 13665.352
Week 132: 13853.641
Week 133: 14044.190
Week 134: 14237.021
Week 135: 14432.154
Week 136: 14629.610
Week 137: 14829.410
Week 138: 15031.574
Week 139: 15236.125
Week 140: 15443.083
Week 141: 15652.469
Week 142: 15864.305
Week 143: 16078.612
```

The following is a comparison of actual and predicted data

![plot](images\3.png)

The accuracy of converting an exponential nonlinear regression mathematical model to predict the production of EGIEaccesibledoor bags.  
The model was converted into numerical form using Taylor Series approach.

Comparison with Actual Data:  
We can compare the approximated production prediction with the actual data for the available period.  
The difference between predictions and actual data can be calculated to see the level of accuracy.  
Visualization of data and predictions can help to see patterns and accuracy more clearly.

From the resulting graph, we can see that the prediction of bag production with the exponential nonlinear regression model is quite accurate in modeling the growth trend of EGIEaccesibledoor bag production. The graph also shows that the actual and predicted data have similar growth patterns, which indicates that this model can be used to predict future bag production.

## Problem 3

    The warehouse was designed to be able to store a maximum of 25,000 (twenty five thousands) bags at each month. Your supervisor asked you to provide a prediction when do EGIER need to build a new warehouse based on the trend that you have acquired in problem #2. To build a new warehouse, it is predicted that they need at least 13 months. So provide the time when EGIER need to start building their new warehouse.

To determine when EGIER should build a new warehouse, we need to know when bag production will exceed the maximum capacity of the warehouse. The maximum capacity of the warehouse is 25,000 bags per month. From the bag production prediction that we have done, we can determine when the bag production will exceed the warehouse capacity.

```python
max_capacity = 25000

def production_prediction(t):
    return P_0 * np.exp(k * t)

def production_prediction_derivative(t):
    return P_0 * k * np.exp(k * t)

def root_function(t):
    return production_prediction(t) - max_capacity

def newton_raphson(root_function, x0, tol=1e-6, max_iter=100):
    x = x0
    for _ in range(max_iter):
        if abs(root_function(x)) < tol:
            return x
        dx = -root_function(x) / production_prediction_derivative(x)
        x += dx
    raise RuntimeError("Maximum iterations reached")

def production_prediction_derivative(t):
    return P_0 * k * np.exp(k * t)

t_predicted = newton_raphson(root_function, 1)

time_to_build = 13
start_building_time = t_predicted - time_to_build
```

The output of the above code produces a prediction of the time when EGIER needs to build a new warehouse is in week 154.

The prediction uses the root square function and the Newton-Raphson method to find the root of the function. In this case, the function used is the difference between the predicted bag production and the maximum capacity of the warehouse. By using the Newton-Raphson method, we can find the time when the bag production exceeds the warehouse capacity.

## Conclusion

The exponential nonlinear regression model is used to predict the trend of EGIEaccesibledoor bag production. The model is converted into numerical form using the Taylor series approach to predict the production of EGIEaccesibledoor bags per week. The prediction shows that EGIEaccesibledoor will need to build a new warehouse in week 154. This prediction is based on the exponential growth trend of bag production and the maximum capacity of the warehouse. By using mathematical models and numerical methods, we can provide accurate predictions for EGIEaccesibledoor bag production and help them plan for future warehouse capacity.

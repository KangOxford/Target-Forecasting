# Time-Series-Forecasting
Trading Target(Volume/Volatility) Time Series Prediction in LOB

Forecasted Trading Volume is crucial in the VWAP replicating strategies and could be used in the [Optimal Execution](https://github.com/KangOxford/AlphaTrade), such as [Optimal Scheduling with Predicted Trading Volume](https://alphatrade.readthedocs.io/en/latest/future_research.html#future-research-topics). We have the [environment: AlphaTrade](https://github.com/KangOxford/AlphaTrade) built in Jax which can automatically paralleling the env and train/testing our algorithm on thousands of stocks at the same time, with a speed up over 100 times.


![sketch](https://user-images.githubusercontent.com/37290277/221001866-667fb755-3dae-4319-9539-99c2197e0e2b.png)


# Timeline:

## Week 2 Feature Engineering
* Target: percentage change of volume
* Imbalance:<br>
  $\frac{x_{bid} - x_{ask}}{x_{bid}+x_{ask}}$
* Lookback window
  * disjoint lookback window
  * overlap lookback window
  
$$
\left\{
             \begin{array}{lr}
             (t-1), & 20 features,   \\
             (t-2) \sim (t-5),&  20 features\\
             (t-6) \sim (t-20),&  20 features, &  
             \end{array}
\right.
$$
  
* Indicators
  * [Implemented Indicators](https://github.com/KangOxford/Volume-Forecasting/blob/new/indicator.md)
* Literature
  * [Order Behavior In High Frequency Markets](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjWh56jmLP7AhXKSsAKHVbGDC8QFnoECA4QAQ&url=https%3A%2F%2Fegrove.olemiss.edu%2Fcgi%2Fviewcontent.cgi%3Farticle%3D1561%26context%3Detd&usg=AOvVaw3f5_VReBN79AwGYPqyOd5C)
  * [Order Exposure in High Frequency Markets](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjWh56jmLP7AhXKSsAKHVbGDC8QFnoECAkQAw&url=http%3A%2F%2Ffaculty.haas.berkeley.edu%2Fhender%2FHidden_AT_HFT.pdf&usg=AOvVaw1SUvGS2w2GWj83ibC4MRSA)
  


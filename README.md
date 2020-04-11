# AAE_Notebook_028_PIDControl
Now that we've looked at PD Control, let's take things a step further to a full PID Controller implementation...

### PID Control

In the previous notebook [AAE_Notebook_027_FeedForward](https://github.com/FadedIllusions/AAE_Notebook_027_FeedForward), if you played around with the mass error variable any at all (with 1.0 being not any error), you noticed that, when we introduce a mass error, we created a systematic bias within the PD Controller.

![Systematic Bias](/images/systematic_bias.png)

To correct for systematic bias, we need a full PID (Proportional-Integral-Derivative) Controller. 

![PID Equation](/images/PID_Equation.png)

If you recalll from calculus, the integral computes the area under the curve -- that is, an accumulated error over time. By introducing and integral term into our control system, we can further adjust the system to account for the accumulation of error over time.

![Reparameterized PID Equation](/images/reparameterized_pid.png)

***   ***   ***   ***   ***   ***   ***   ***   ***

### PD Tuning Considerations

If you don't want to think about delta and time constant, you can refer to the table below, which shows what to expect when tuning a system directly tweaking the values of Kp, Kd, Ki.

![PID Tuning Considerations](/images/pid_considerations.png)

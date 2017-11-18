# iir_filters
iir filters ROS wrapper with C++.

This repository wrapper the origin [IIR filters repository](https://github.com/berndporr/iir1) for ROS.

> This is a powerful filter library which implements all
standard IIR filters such as Bessel, Butterworth,
Elliptic and Chebychev. The data format is
floating-point throughout.

# Usages
Just copy this repository as a stanalone ROS package in your catkin workspace.

In your project, use the filter like this
```cpp
// init filter
Iir::Butterworth::LowPass<order> f;  // NOTE： here order should replaced by a int number!
const float samplingrate = 1000; // Hz
const float cutoff_frequency = 5; // Hz
f.setup (order, samplingrate, cutoff_frequency); // NOTE： here order should replaced by a int number!

// Realtime filtering sample by sample
float y = f.filter(x); // here x is a float, and one dimension
```

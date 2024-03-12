# Tutorial Reflections
## Name: Muhammad Sean Arsha Galant
## NPM: 2206822963
__________________________________________

# Module 5
## GUI Test plan result for /all-student-name
![Screenshot 2024-03-10 142756.png](assets%2FScreenshot%202024-03-10%20142756.png)
![Screenshot 2024-03-10 142803.png](assets%2FScreenshot%202024-03-10%20142803.png)
![Screenshot 2024-03-10 142810.png](assets%2FScreenshot%202024-03-10%20142810.png)
![Screenshot 2024-03-10 142815.png](assets%2FScreenshot%202024-03-10%20142815.png)

## GUI Test plan result for /highest-gpa
![Screenshot 2024-03-10 142629.png](assets%2FScreenshot%202024-03-10%20142629.png)
![Screenshot 2024-03-10 142643.png](assets%2FScreenshot%202024-03-10%20142643.png)
![Screenshot 2024-03-10 142653.png](assets%2FScreenshot%202024-03-10%20142653.png)
![Screenshot 2024-03-10 142708.png](assets%2FScreenshot%202024-03-10%20142708.png)

## Command-line test plan result for /all-student-name
![Screenshot 2024-03-10 144700.png](assets%2FScreenshot%202024-03-10%20144700.png)
![Screenshot 2024-03-10 144759.png](assets%2FScreenshot%202024-03-10%20144759.png)

## Command-line test plan result for /highest-gpa
![Screenshot 2024-03-10 144829.png](assets%2FScreenshot%202024-03-10%20144829.png)
![Screenshot 2024-03-10 144841.png](assets%2FScreenshot%202024-03-10%20144841.png)

## Before Optimization
## /all-student-name
![Screenshot 2024-03-10 144700.png](assets%2FScreenshot%202024-03-10%20144700.png)
![Screenshot 2024-03-10 144759.png](assets%2FScreenshot%202024-03-10%20144759.png)
![Screenshot 2024-03-10 160921.png](assets%2FScreenshot%202024-03-10%20160921.png)
![Screenshot 2024-03-10 161939.png](assets%2FScreenshot%202024-03-10%20161939.png)

## /highest-gpa
![Screenshot 2024-03-10 144829.png](assets%2FScreenshot%202024-03-10%20144829.png)
![Screenshot 2024-03-10 144841.png](assets%2FScreenshot%202024-03-10%20144841.png)
![Screenshot 2024-03-10 162443.png](assets%2FScreenshot%202024-03-10%20162443.png)
![Screenshot 2024-03-10 162343.png](assets%2FScreenshot%202024-03-10%20162343.png)
__________________________________________
## After optimization
## /all-student-name
![Screenshot 2024-03-10 164013.png](assets%2FScreenshot%202024-03-10%20164013.png)
![Screenshot 2024-03-10 164253.png](assets%2FScreenshot%202024-03-10%20164253.png)
![Screenshot 2024-03-10 161859.png](assets%2FScreenshot%202024-03-10%20161859.png)
![Screenshot 2024-03-10 161933.png](assets%2FScreenshot%202024-03-10%20161933.png)

## /highest-gpa
![Screenshot 2024-03-10 164243.png](assets%2FScreenshot%202024-03-10%20164243.png)
![Screenshot 2024-03-10 164257.png](assets%2FScreenshot%202024-03-10%20164257.png)
![Screenshot 2024-03-10 163432.png](assets%2FScreenshot%202024-03-10%20163432.png)
![Screenshot 2024-03-10 163527.png](assets%2FScreenshot%202024-03-10%20163527.png)

## Conclusion for comparison
After running the performance tests again using JMeter, we can observe that there are results compared to the first measurement. For the endpoint /all-student-name, it took 7 seconds to complete 10 requests with 1.4 requests made per second in JMeter prior to optimization, and took 1 second to carry out 10 requests after optimization with 8.4 requests per second (significantly higher!). We can also see that the average response time (Avg), minimum response time (Min), and maximum response time (Max) has all reduced greatly
after optimization from the thousands of milliseconds to only hundreds of milliseconds. This is obviously more than a 20% performance improvement. Conversely, for the /highest-gpa endpoint, we can also see that it took 10 requests made per second in both prior and after optimization, however, the rate of requests made per second increased drastically from 9.8 requests per second to 10.7 requests per second. The Avg, Min, and Max response times could also be observed to reduce.
## Reflection for Module 5
1. What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?

JMeter and IntelliJ Profiler take different approaches to application performance optimization. JMeter simulates real-world user loads on your application, stressing it under controlled conditions. It measures things like response times, throughput, and resource usage at the system level. This helps identify if the application meets performance benchmarks or if there are bottlenecks under heavy use. 
On the other hand, IntelliJ Profiler focuses on pinpointing performance issues within your application's code. It analyzes how the application behaves during execution, identifying which parts of the code take the most time or memory. This helped me pinpoint specific methods or functionalities that need improvement. 
In essence, JMeter tells you if your application is fast enough for real-world use, while IntelliJ Profiler helps you identify why it might be slow and where to optimize the code itself. They work together effectively - JMeter highlights performance problems, and IntelliJ Profiler helps me diagnose and fix them. 

2. How does the profiling process help you in identifying and understanding the weak points in your application?

Profiling is a crucial process in identifying and understanding weak points in an application's performance. Profiling allows for the examination of various aspects such as CPU usage, memory consumption, and thread activity. For example, with IntelliJ's Profiler, I can identify specific methods or functions that consume a disproportionate amount of resources, contributing to performance bottlenecks. Profiling aids in the detection of inefficient algorithms, memory leaks, or excessive object creation, providing a precise view of where the application may be under-performing.
Moreover, profiling helps uncover the intricacies of thread interactions, revealing potential contention issues that could lead to performance degradation. The collected data allows developers to analyze the call stack, method timings, and memory allocations, enabling them to make informed decisions about optimizations.

3. Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?

Yes, IntelliJ Profiler is effective in assisting me analyze and identify bottlenecks in my application code. By using features such as method profiling, I could pinpoint specific functions or methods that contribute significantly to the application's execution time. The profiler also facilitates the detection of memory leaks, excessive object creation, and inefficient algorithms, allowing me to address these issues directly in my code. It also provides a visual representation of the call stack and method timings which allows me to visualize the execution flow and understand where the code spends the most time.
The Profiler's ability to capture real-time data during application execution also provided me with a dynamic and accurate assessment of performance bottlenecks.

4. What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?

The main challenges I faced when conducting performance testing include trying to understand the results given from the test and also waiting for the tests to complete, especially for the /all-student endpoint. I struggled initially with trying to understand the results/data provided from the tests from either JMeter or IntelliJ Profiler because I did not understand how to interpret some graphs at first such as the flame graph given in the IntelliJ Profiler or the summary of results given from JMeter in the command-line. To overcome these issues, I re-read the module on how to interpret flame graphs, where I found out each block on the graph represents a function in the stack, with the width indicating the function's relative execution time (and call paths as wider, "hotter" flames),
and the section in the module about JMeter where it discusses how to analyze the summary of results given such as general statistics, response time distribution, throughput, and error percentage. As for the issue of waiting for the /all-student tests to complete, the only way I could overcome this was to optimize the code in the StudentService.java, which significantly reduced the time from approximately 4 minutes to carry out the tests to only less than a minute to carry it out on JMeter (or even the IntelliJ Profiler).

5. What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?

Firstly, te IntelliJ Profiler provides detailed insights into the runtime behavior of my application that allowed me to identify and analyze performance bottlenecks, memory leaks, and inefficient code segments. This visibility aids in understanding the execution flow and resource utilization, facilitating targeted improvements. Another advantage is the real-time data visualization and interactive interface. This interactivity fosters a more intuitive and efficient debugging process, allowing for on-the-fly adjustments and deeper investigation into specific areas of concern. 
Additionally, the profiler integrates seamlessly with the IntelliJ IDEA development environment, streamlining well with my workflow and enhancing the overall testing and optimizing experience.

6. How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?

First and foremost, it's essential to scrutinize the differences in the environments and methodologies employed by each tool. IntelliJ Profiler typically provides detailed insights into the runtime behavior of a specific application during development, whereas JMeter focuses on simulating user interactions under various loads in a controlled testing environment. Discrepancies may arise due to variations in data sets, test scenarios, or the distinct nature of these tools.
To address these discrepancies, I validated and aligned the performance testing configurations, ensuring that both tools are analyzing the application under comparable and similar conditions as much as possible. For example, for JMeter I modified the settings of the Thread Group so that it matches with the settings of the IntelliJ Profiler so that the tests could remain consistent. I also conducted testing before and after optimization for each feature using both JMeter and 
the IntelliJ Profiler to see if there are any further discrepancies, and if there are, I tried to improve my code further or tried to tweak the settings of each performance/testing suite so that they are aligned.

7. What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?

After analyzing results from performance testing and profiling, I try to observe which part of the program (such as the method or line in the program) is taking the most resources to process in the test/profiling process. After I identify the main source of the performance issue through the flame graph and method list provided in IntelliJ Profiler, as well as the number of requests per second it took from JMeter, I locate the method in which I need to optimize and improve its performance upon. This correlates with the next step, that is through continuous testing with my improvements/changes made to the code. Continuous testing, especially with performance benchmarks and load testing scenarios, helps monitor the impact of changes and ensures improvements align with performance goals.
To ensure the changes you make do not affect the application's functionality, I observed the output created before the change/optimization and after the change/optimization. To do this, I used Postman (as observed from the screenshots above) to see the output of each request made to the endpoints (/all-student-name, /highest-gpa, /all-students) before and after refactoring. If the output made is different from before the refactoring process, that means I have changed the application's functionality. On the other hand, if the output is the same after refactoring with the output before refactoring, and is completed in significantly less time to process the request, then I have optimized the code correct and ensured that the functionality of the application has remained the same.
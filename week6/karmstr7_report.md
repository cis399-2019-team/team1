## Week 6 Assignment Deliverables

### CPU Utilization Alarm 
    Alarm Details:
    - Name:                       awsec2-i-0ee32fb0b84039d83-CPU-Utilization
    - Description:                Created from EC2 Console
    - State Change:               OK -> ALARM
    - Reason for State Change:    Threshold Crossed: 1 datapoint [95.48596832453458 (02/08/19 04:23:00)] was greater than or equal to the threshold (95.0).
    - Timestamp:                  Friday 02 August, 2019 04:28:38 UTC
    - AWS Account:                006170570170

    Threshold:
    - The alarm is in the ALARM state when the metric is GreaterThanOrEqualToThreshold 95.0 for 300 seconds.

    Monitored Metric:
    - MetricNamespace:                     AWS/EC2
    - MetricName:                          CPUUtilization
    - Dimensions:                          [InstanceId = i-0ee32fb0b84039d83]
    - Period:                              300 seconds
    - Statistic:                           Average
    - Unit:                                not specified
### Network In Alarm
    Alarm Details:
    - Name:                       awsec2-i-0ee32fb0b84039d83-High-Network-In
    - Description:                Created from EC2 Console
    - State Change:               OK -> ALARM
    - Reason for State Change:    Threshold Crossed: 1 datapoint [4984793.2 (02/08/19 04:38:00)] was greater than or equal to the threshold (500000.0).
    - Timestamp:                  Friday 02 August, 2019 04:43:51 UTC
    - AWS Account:                006170570170

    Threshold:
    - The alarm is in the ALARM state when the metric is GreaterThanOrEqualToThreshold 500000.0 for 300 seconds.

    Monitored Metric:
    - MetricNamespace:                     AWS/EC2
    - MetricName:                          NetworkIn
    - Dimensions:                          [InstanceId = i-0ee32fb0b84039d83]
    - Period:                              300 seconds
    - Statistic:                           Average
    - Unit:                                not specified

### Network Out Alarm
    Alarm Details:
    - Name:                       awsec2-i-0ee32fb0b84039d83-High-Network-Out
    - Description:                Created from EC2 Console
    - State Change:               OK -> ALARM
    - Reason for State Change:    Threshold Crossed: 1 datapoint [73006.6 (02/08/19 04:03:00)] was greater than or equal to the threshold (50000.0).
    - Timestamp:                  Friday 02 August, 2019 04:08:31 UTC
    - AWS Account:                006170570170

    Threshold:
    - The alarm is in the ALARM state when the metric is GreaterThanOrEqualToThreshold 50000.0 for 300 seconds.

    Monitored Metric:
    - MetricNamespace:                     AWS/EC2
    - MetricName:                          NetworkOut
    - Dimensions:                          [InstanceId = i-0ee32fb0b84039d83]
    - Period:                              300 seconds
    - Statistic:                           Average
    - Unit:                                not specified

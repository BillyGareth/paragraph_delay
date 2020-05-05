# paragraph_delay
Description
Python time method sleep() suspends execution for the given number of seconds. The argument may be a floating point number to indicate a more precise sleep time.

The actual suspension time may be less than that requested because any caught signal will terminate the sleep() following execution of that signal's catching routine.

## The Accuracy of time.sleep()
The time.sleep() function uses the underlying operating system's sleep() function. Ultimately there are limitations of this function. For example on a standard Windows installation, the smallest interval you may sleep is 10 - 13 milliseconds. The Linux kernels tend to have a higher tick rate, where the intervals are generally closer to 1 millisecond. Note that in Linux, you can install the RT_PREEMPT patch set, which allows you to have a semi-realtime kernel. Using a real-time kernel will further increase the accuracy of the time.sleep() function. Generally however, unless you want to sleep for a very small period, you can generally ignore this information.

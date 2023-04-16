# function_placement

function_placement is a tool to optimize the placement of serverless functions on a distributed computing infrastructure. The tool provides a solution to the problem of assigning functions to servers in order to minimize the overall response time of the system. This problem arises when deploying serverless applications in large-scale distributed systems with heterogeneous resources.

# Prerequisites
In order to use function_placement, you need to have the following software installed:

Python 3
NumPy
Pandas

# Installation

I. Create SUT
II. Run Load Genertor
To install function_placement, clone the repository and install the dependencies using pip:

git clone https://github.com/ankushshr1993/function_placement.git
cd function_placement
pip install -r requirements.txt

# Usage
To use function_placement, you need to provide a configuration file in YAML format, which specifies the functions and the servers in the system, as well as their performance characteristics. An example configuration file is provided in the examples directory.

Once you have a configuration file, you can run function_placement by executing the following command:
python3 load_generator.py <function_name> <Series/Parallel> <Number of invocation> <Type of Algorithm>

The algorithm parameter specifies the algorithm to use for function placement. Currently, the following algorithms are supported:

function_name: the name of the serverless function you want to load test.
Series/Parallel: specifies whether you want to invoke the function in series or parallel. If you choose "Series", each invocation will be completed before the next one begins. If you choose "Parallel", all invocations will be started at the same time.
Number of invocations: the total number of invocations you want to make on the function.
Type of Algorithm: specifies the type of algorithm you want to use for node placement. This can be either "kalman", "extended", or "particle".
After running the load test, the tool will output the total execution time and also write the invocation timestamps to a CSV file named "loaddata.csv" in the same directory as the tool.







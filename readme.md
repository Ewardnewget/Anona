# Dysmo


## The Tool Dysmo

The file "tool.so" is the binary file of Dysmo. It requires LLVM+Clang 7.1.0.

To use it, you need first get the IR file of the tested program, and the trace files.

Run the following command to analyze the traces:
```
opt -load ./tool.so -vulana -tpath PATH_TO_TRACES -maxm=xx -maxt=xx PATH_TO_IR_FILE
```
For example, using the following command to analyze the traces in folder "example":
```
opt -load ./tool.so -vulana -tpath ./example -maxm=8 -maxt=1 ./example/test.bc
```
Use the paramters "maxm" and "maxt" specify the maximum memory (in GB) and the number of threads running concurrently，which in default are "8GB" and "1" thread.

## The Experiment Logs

The result logs from experiments are provided in Result.zip.

There are 22 folders named with the names of test suites in MySQL. 

In each folder,"ORRD_0.log"  and "ORRD_resource.log" are the log files of Dysmo, and  "SeqTocc_0.log"  and"SeqTocc_resource.log" are the log files of M2 and SeqCheck.


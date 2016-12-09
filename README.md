# HadoopStreamingAPI

## The instructions for data analysis on hadoop server which supports HadoopStreamingAPI are given below

Clone this repository first

After cloning is done, run the below command on hadoop cluster by changing output path

hadoop jar /usr/local/hadoop/share/hadoop/tools/lib/hadoop-streaming-2.7.1.jar -input /data/nyc/nyc-traffic.csv -output /users-cloud-16fs/ballima/output/job1-out/o1 -mapper ~/mapper.py -reducer ~/reducer.py -file ~/{mapper,reducer}.py
 
After execution of hadoop jobs, the output can be viewed in hdfs using below command
 
hdfs dfs -cat /users-cloud-16fs/ballima/output/job1-out/o1/part-00000

The output which gives the statistics for the input data is below:
  
AMBULANCE 3713

BICYCLE 24153

BUS 25871

FIRE TRUCK 1333

LARGE COM VEH(6 OR MORE TIRES) 27981

LIVERY VEHICLE 17775

MOTORCYCLE 10029

OTHER 51360

PASSENGER VEHICLE 1005162

PEDICAB 123

PICK-UP TRUCK 26281

SCOOTER 534

SMALL COM VEH(4 TIRES) 30048

SPORT UTILITY / STATION WAGON 363209

TAXI 63892

UNKNOWN 105481

VAN 51666

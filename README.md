# erl-perfomance-scripts

1.	Run scripts in “headless” mode
2.	Pass user/thread count as a parameter from command line
3.	Modify existing script and alter Think times / Assertions / Timeouts 

# Requirements:
1. Apache JMeter 5.3
2. Java 8 +
3. Data Files (vehicle numbers per each province and users per each province)
Ex: westernusers.csv , western.csv ( These files should be placed in a folder named ‘Data’ inside the bin folder of Jmeter installation


# Running the jmeter script 

1. The scripts and data files available in following repository 
   (https://github.com/ICTASL/erl-perfomance-scripts )
   [Four scripts available in the repo erl-plan-300.jmx , erl-plan-350.jmx , erl-plan-400.jmx,department.jmx ]

  #### Ex : If the performance test need to be conducted with 300 users  

   `jmeter -n -t <script_name.jmx>   -l <logname.jmx>`
  
    ex: `jmeter -n -t erl-plan-300.jmx   -l mylog.jtl`
   
    The results will be saved in mylog.jtl

  #### Or can use department.jmx and specify user count in command line (per each province)
 
`jmeter -n -t  department.jmx   -Jwusers=100 -Jcusers=50 -Jnusers=50 -Jnesers=50 -Jncusers=50 –l  resultslog.jtl`




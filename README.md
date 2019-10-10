# CCOM3986: Network Security Visualizations
> Dianelys Soto-Cruz
> Prof. Jose Ortiz-Ubarri
> CCOM 3986

## Table of contents
- [Description](#description)
-  [Screenshots](#screenshots)
- [Prerequisites](#prerequisites)
- [How to use](#how-to-use)
- [Author](#author)

## Description
As my first research experience, I'm currently working on developing a web-based system that would provide anomaly detection from port scanning threats through visuals. This is being done with a Python script that parses NetFlow data generated by the High Performance Computing Facility of the University of Puerto Rico. It  then generates JSON data that is used to render a stacked bar graph of commonly used ports per hour of a day done by using JavaScript d3 library. Further optimization and visuals are being worked including a heatmap calendar.

## Prerequisites
1. Web server
2. NetFlow generated data
3. Python
4. SiLK 
5. Cron job scheduler


## How to use
FLOW-DATA.py
* Variable _startDate_ the user can determine an which date to start reading flows files. 
    
    _ie. datetime(2018, 1, 1, 0)_

* Variable _endDate_ the user can determine an which date to stop reading flows files. 

    _ie. datetime(2019, 11, 25, 23)_
    
* Variable _site_config_file_ should be assigned to SiLK configuration file. 

    _ie. "/etc/silk/conf-v9/silk.conf"_
    
* Variable _data_rootdir_ should be assigned to NetFlow data directory.

    _ie. "/home/scratch/flow/rwflowpack/"_

UPDATE-DATA.py
* Variable _startDate_ the user must determine the date on which to start reading flows files. Should be the day right after _endDate_ on FLOW-DATA.py  file.
    
    _ie. datetime(2019, 11, 26, 0)_

* Variable _endDate_ the user must determine the date on which to stop reading flows files. Should be the day right after the previously stablished _startDate_.

    _ie. datetime(2019, 11, 27, 23)_ 
    

## How to execute the process
To run the programs: 
1) First, run FLOW-DATA.py to start collecting and parsing flow data. 
    ```sh
    $ python FLOW-DATA.py & 
    ```
2) After, the job is done executing. Run crontab to add job scheduling for UPDATE-DATA.py.
    ```sh
    $ crontab -e 
    ```

3)  tba
    ```sh
    $ tba
    ```
4) tba

## Author
Created by Dianelys Soto-Cruz

## References

1. Python
2. SiLK
3. JavaScript d3
4. Crontab


[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [AngularJS]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>

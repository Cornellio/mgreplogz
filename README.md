# Mgreplogz

This is a basic utility for searching Tomcat server logs that provides:

- looping through multiple servers
- searching compressed log files (using zgrep)
- searching subdirectories by given date

# Usage

Run `./mgreplogz` by itself to show usage

Example: To grep for ip address 46.105.144.23 on the given servers, searching only the web log file pattern `web3-2017-06-13-07-1*`

    ./mgreplogz -h "webapi01 webapi02 webapi03" -f web3-2017-06-13-07-1* 46.105.144.23

    Searching hosts: webapi01 webapi02 webapi03
    Search pattern: 46.105.144.23   /var/log/tomcat/2017-06-13/web3-2017-06-13-07-1*
    Writing results to: ~/log_search_output_2017-06-13_1605

    ...webapi01
    ...webapi02
    ...webapi03

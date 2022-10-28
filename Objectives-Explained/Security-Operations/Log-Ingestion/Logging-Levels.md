# Logging Levels

## Explanation

- log level = log severity; how important a log is relative to others
- common log levels:
    - TRACE = verbose tracking for deep insight into system activity
    - DEBUG = used for troubleshooting in test env
    - INFO = what happened and when; not indicative of a problem, just system status
    - WARN = unexpected problem occurred, something didn't work right, but the system as a whole keeps working 
    - ERROR = loss of functionality
    - FATAL = something really important broke, and now the business is suffering

## Importance

- helps prevent alert fatigue
    - if FATAL logs are treated by the system the same as TRACE logs, analysts wouldn't be able to see through all the noise

## Example

| Log Level | Example |
| --------- | ------- |
| TRACE | File writes, method/file execution |
| DEBUG | Content of DB/file writes, variable values at key points |
| INFO | User login, session timeout |
| WARN | Error parsing file | 
| ERROR | One of several payment systems is unavailable |
| FATAL | User login service disabled |

## Additional Resources

- [Sematext](https://sematext.com/blog/logging-levels/)
- [Crowdstrike](https://www.crowdstrike.com/cybersecurity-101/observability/logging-levels/)
- [Section](https://www.section.io/engineering-education/how-to-choose-levels-of-logging/)
- [IBM](https://www.ibm.com/docs/en/cognos-analytics/10.2.2?topic=SSEP7J_10.2.2/com.ibm.swg.ba.cognos.ug_rtm_wb.10.2.2.doc/c_n30e74.html)
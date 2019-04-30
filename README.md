[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.tperamaki/log4j-json-layout/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.tperamaki/log4j-json-layout/)

# Log4J JSON Layout
A JSON layout for Log4J (v1.2).

## Output format
```
{"timestamp":"<DATE>","level":"<LEVEL>","logger":"<LOGGER>","thread":"<THREAD>","message":"<MESSAGE>","stacktrace":"<STACKTRACE>"}
```
The "stacktrace" item is optional and will only be in the JSON object if the log message has a trace message.

## Example log4j.properties
```
log4j.appender.stdout=org.apache.log4j.ConsoleAppender
log4j.appender.stdout.layout=org.apache.log4j.PatternLayout
log4j.appender.stdout.layout=com.tperamaki.log4j.JsonLayout
log4j.appender.stdout.layout.ConversionPattern=[%d] %p %m (%c)%n
log4j.appender.stdout.layout.DatePattern=yyyy-MM-dd'T'HH:mm'Z'
```

## Layout configuration
| Name | Options | Default |
|------|---------|---------|
| DatePattern | all valid SimpleDateFormat patterns | yyyy-MM-dd HH:mm:ss,SSS |

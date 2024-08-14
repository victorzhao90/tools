<configuration>
    <!-- Define a file appender with a timestamp in the file name -->
    <appender name="FILE" class="ch.qos.logback.core.FileAppender">
        <file>logs/app-%d{yyyy-MM-dd}.log</file> <!-- Timestamp format for file name -->
        <encoder>
            <pattern>%d{yyyy-MM-dd HH:mm:ss} [%thread] %-5level %logger{36} - %msg%n</pattern>
        </encoder>
    </appender>

    <!-- Root logger configuration -->
    <root level="info">
        <appender-ref ref="FILE"/>
    </root>
</configuration>
this is a readme

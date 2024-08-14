<configuration>
    <!-- Define a rolling file appender with a timestamp in the file name -->
    <appender name="FILE" class="ch.qos.logback.core.rolling.RollingFileAppender">
        <file>C:/files/logs/app.log</file>
        <rollingPolicy class="ch.qos.logback.core.rolling.TimeBasedRollingPolicy">
            <fileNamePattern>C:/files/logs/app-%d{yyyy-MM-dd}.%i.log</fileNamePattern>
            <maxHistory>30</maxHistory>
            <totalSizeCap>10GB</totalSizeCap>
        </rollingPolicy>
        <encoder>
            <pattern>%d{yyyy-MM-dd HH:mm:ss} [%thread] %-5level %logger{36} - %msg%n</pattern>
        </encoder>
    </appender>

    <!-- Root logger configuration -->
    <root level="info">
        <appender-ref ref="FILE"/>
    </root>
</configuration>

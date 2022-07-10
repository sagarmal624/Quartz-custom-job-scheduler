# Spring Boot Quartz Scheduler Example: Building an Email Scheduling app

**Complete Tutorial:** https://www.callicoder.com/spring-boot-quartz-scheduler-email-scheduling-example/

## Requirements

1. Java - 11

2. Maven - 3.x.x

3. MySQL - 5.x.x

## Steps to Setup


**6. Build and run the app using maven**

Finally, You can run the app by typing the following command from the root directory of the project -

```bash
mvn spring-boot:run
```

## Scheduling an Email using the /scheduleEmail API

```bash
curl --location --request POST 'localhost:8081/scheduleEmail' \
--header 'Content-Type: application/json' \
--data-raw '{
    "email": "sagarmal624@gmail.com",
    "subject": "Things I wanna say to my Future self",
    "body": "Dear Future me, <br><br> <b>Think Big And Don’t Listen To People Who Tell You It Can’t Be Done. Life’s Too Short To Think Small.</b> <br><br> Cheers, <br>Rajeev!",
    "dateTime": "2022-07-10T18:20:00",
    "timeZone": "Asia/Kolkata",
    "cron":"0 0/1 18-19 * * ?"
}'

# Output
{"success":true,"jobId":"0741eafc-0627-446f-9eaf-26f5d6b29ec2","jobGroup":"email-jobs","message":"Email Scheduled Successfully!"}
```
#CS #FTC
An open Control loop means that giving a specific output without checking it based on the input. A basic example of this is that of a time-based autonomous:
```java
// Start motors at desired speed
frontLeft.setPower(1);
frontRight.setPower(1);
backLeft.setPower(1);
backRight.setPower(1);

// Leave motors running for desired time
sleep(500);

// Stop motors after desired time
frontLeft.setPower(0);
frontRight.setPower(0);
backLeft.setPower(0);
backRight.setPower(0);
```
Another example of open loop control is that of an intake which runs continuously:
```java
// Set intake power at max output
intakeMotor.setPower(1);
```
![](https://1690765679-files.gitbook.io/~/files/v0/b/gitbook-legacy-files/o/assets%2F-MU2Qk3INKAMMgKbsAgJ%2F-MXnkL22CgInq5666w_H%2F-MXnmVfxj2n3lfGBYDsQ%2FScreen%20Shot%202021-04-08%20at%207.20.35%20PM.png?alt=media&token=90054a91-5df7-4cd6-81e9-8cc6f3f37ad0)
Open loop control is an incredibly simple way to get a robot performing actions. Unfortunately, this method has a few critical downfalls for certain systems:
- Cannot reject disturbances
	- Cannot overcome contact from other robots
- Energy inefficient
	- Motors must run at maximum power to utilize their maximum torque potential
- Consistency will vary as battery voltage changes.
These downfalls really only matter for certain types of systems. For example, your intake doesn't really need to reject disturbances from the outside world like your drivetrain does. This means that choosing Open Loop Control vs [[Closed Loop Control]] is decided with personal preference and the ***design requirements*** of your system.
>[!definition] Design Requirements
>What your system needs to accomplish.
>Does it need to reject disturbances? Does it need to be fast? Can it be slow? How accurate does it need to be? All of these things are factored into your system's ***design requirements***.

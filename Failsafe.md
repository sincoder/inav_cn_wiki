# Setting up Failsafe for RTH

## Forewords

The goal is to configured both your flight controller and radio receiver so failsafe does as expected in every situation.

For failsafe to work optimal iNav needs to know it's in a failsafe event and not just doing regular RTH. This is for example correctly handle loss of GPS while returning to home.

Also this assumes you have regular GPS modes like `RTH` working already.

### Configuration of receiver

One got two options on how to configure receiver.

**Option one**

Set receiver to send out `NO PULSES` on a failsafe event.

**Option two**

1. In `Modes` tab select a switch for "Failsafe"

1. Set your switches and sticks of your radio to the following conditions:  

 `Throttle: approx. 0% (no throttle)`  

 `Aileron: 50% (no input, stick center)`  

 `Rudder: 50% (no input, stick center)`  

 `Elevator: 50% (no input, stick center)`  

 `Failsafe mode: activated`  

 `Arm switch: Disarmed (If you use stick arming you can skip this)`  

1. Configure failsafe on your receiver to the above conditions on link loss (consult manual for your receiver on how to do it)

### Configuration of iNav

Go to `Failsafe` tab, and enable `RTH` as Stage 2 failsafe.

Behavior of RTH can also be configured.
 - [iNav Flight modes / Navigation Modes](/iNavFlight/inav/wiki/Navigation-modes#rth-altitude-control-modes)

### Verifying that failsafe works as intended

Verify that your failsafe works.

* Remove all props  

* Go outside, arm and apply throttle, walk with it 20meter away from home (normally the place where you armed it) and then turn off transmitter. The aircraft should now try to climb (increase throttle). Also verify that you're able to regain control by turning on transmitter again, and move the ROLL/PITCH stick more than.  

* Real test: Take the props on again. Take off, fly at least 20 meters from home, and turn off transmitter. Tip: Do this over soft grass. If it's an airplane it's better to have some altitude.  

Note: If you are using fixedwing without magnetometer enabled you will need to run with airplane before turning off transmitter to test failsafe. This is because GPS speed needs to be above a certain threshold to aquirre a valid heading. Without a valid heading failsafe will not initated.

Note: To regain controll after failsafe event `failsafe_stick_threshold` is default turned on, and requirres you to move the Roll/pitch sticks to regain control.  

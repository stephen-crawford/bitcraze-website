---
layout: page-left-menu
title: FAQ
page_id: support-frequently-asked-questions
redirects:
  - /frequently-asked-questions-Crazyflie-2.0/
---

{% si_intro  For how long can the Crazyflie 2.x fly? %}

A Crazyflie 2.x with brushed motors can fly up to 7 minutes, depending on usage.
The Crazyflie 2.1 Brushless version typically flies longer, with an expected flight time of up to 10 minutes, also depending on flying conditions.

{% endsi_intro %}





{% si_intro  How is the Crazyflie 2.x charged? %}
It is charged using a standard micro-USB connector commonly used by smartphones. You probably have one of these cables at home. You can charge it from any USB unit that can supply 500mA, most computers and adapters do. It takes up to 40min to charge and the blue LED (M3) will tell you roughly how charged it is by how long it is lit. When it is fully lit it is fully charged.
{% endsi_intro %}

{% si_intro Can I hot swap batteries on the Crazyflie 2.x? %}
Yes, you can hot swap batteries.
{% endsi_intro %}

{% si_intro Can I use a bigger battery on the Crazyflie 2.x? %}
Yes, as long as it is not too heavy, it is a single cell (3.7V), it fits and the polarity is correct you can do so. A higher capacity battery will give you longer flight times but will decrease agility. We recommend batteries with at least 15C continuous discharge rate.
{% endsi_intro %}

{% si_intro What radio is used with the Crazyflie 2.x? %}
The Crazyflie 2.x can be controlled with the Crazyradio, Crazyradio PA or {% poplink crazyradio-2-0 %} from a PC or with a mobile device using Bluetooth Low Energy.
{% endsi_intro %}

{% si_intro Which mobile devices work with the Crazyflie 2.x? %}
Here is a list of requirements for the mobile device:

* Bluetooth Low Energy (BLE) or sometimes called Bluetooth Smart support.
* Runs Android 4.4 or newer
* Runs iOS 7.1 or newer

Since Android is available on many different devices, it is not certain it works even though it fulfills the requirements above. We have therefore created a [list of devices](/documentation/repository/crazyflie-android-client/master/userguides/user-instructions/#android-device-compatibility)
it has been tested on.
{% endsi_intro %}

{% si_intro What is the range of the Crazyradio? %}
As with all radio communication it depends. It depends on the environment, radio interference, chip production variations, etc. It also depends on if you use the Crazyradio 2.0, Crazyradio PA or a mobile device. We have done a couple of line-of-sight tests with little interference outdoor with the different configurations:

* Crazyradio PA: Up to about 1000 meters range with direct line of sight in the 250 Kbit mode and under ideal conditions (the downlink is the main limiting factor).
* Mobile device: Up to about 20 meters range (The uplink, the mobile device is limiting the range).
{% endsi_intro %}

{% si_intro Can I use a normal R/C transmitter to control the Crazyflie 2.x? %}
This can be done with the [BigQuad expansion deck](/products/bigquad-deck/). It's working, but not yet a turn-key solution.


{% endsi_intro %}

{% si_intro Can I add sensors to my Crazyflie? %}
The expansion ports on the Crazyflie 2.X enables you to connect more or less any hardware you like. When prototyping the [Breakout deck](/products/breakout-deck/) is useful as you can use it to connect your Crazyflie 2.X to a breadboard and easily debug your hardware design. When satisfied with the design you can transfer it to a [prototyping deck](/products/prototyping-deck/) for a more permanent implementation.

{% endsi_intro %}

{% si_intro Can the Crazyflie 2.x fly autonomously? %}
The Crazyflie 2.x does not have enough sensors to locate itself in the environment as is, it requires more information to do that.
The easiest way to achieve that is to add the {% poplink flow-deck %}. It tells the Crazyflie how it moves relative to the floor and
thus enables it to fly autonomously. See the [product page](/products/flow-deck-v2/) for more information.

With an external positioning system the Crazyflie will even understand its absolute
position which gives it even more possibilities when it comes to autonomous flight.
Outdoors the Crazyflie could use a GPS receiver to achieve autonomous flight but indoors some other positioning system is required. Please check out our [positioning system overview page](/documentation/system/) to get know the different possiblities for position available to the Crazyflie.
{% endsi_intro %}

{% si_intro How many base stations do I need to fly in the Lighthouse positioning system? %}
The recommended minimum number of base stations is two. This covers a 5x5x5m area. This can be scaled up to 4 base stations. 
{% endsi_intro %}

{% si_intro How many loco nodes do I need to fly in the Lighthouse positioning system? %}
A theoretical minimum of 4 Anchors is required to calculate the 3D position of a Tag, but a more realistic number is 6 to add redundancy and accuracy.  

{% endsi_intro %}


{% si_intro Can I store data on my Crazyflie? %}
The [SD-card deck](/products/micro-sd-card-deck/) can be used to store configuration data for a Crazyflie. An example could be an autonomous implementation where the Crazyflie is not connected via radio. The configuration can be written to a SD-card in a computer and the SD-card is transferred to the Crazyflie before it is started. This is also a way to separate configuration from hardware/firmware and avoid flashing different firmware to Crazyflie individuals.

{% endsi_intro %}

{% si_intro How durable is the Crazyflie 2.x? %}
The Crazyflie 2.x family, including the Crazyflie 2.1 Brushless, uses the PCB as the frame, made of strong and lightweight [FR4](https://en.wikipedia.org/wiki/FR-4) material.

For the standard Crazyflie 2.x, brushed motors are mounted in flexible motor mounts designed to absorb impact. In a crash, propellers and motor mounts are the most likely components to need replacement. Both are inexpensive and easy to replace. In testing, Crazyflie 2.x drones have survived falls from heights up to 30 meters onto concrete, with damage typically limited to the propellers, motor mounts, or motors. However, it is not unbreakable, so handle with care!

The Crazyflie 2.1 Brushless has brushless motors directly screwed onto the PCB without separate mounts. It includes flexible landing feet or optional motor guards to help absorb impacts. The brushless motors are highly durable and are less prone to breakage, though care is recommended for optimal long-term performance.
{% endsi_intro %}

{% si_intro Can the Crazyflie 2.x be used to control a bigger quadcopter? %}
Yes, it can. With the [BigQuad expansion deck](/products/bigquad-deck/).

You can also consider using the [Crazyflie Bolt 1.1](/products/crazyflie-bolt-1-1/) autopilot board to build an custom drone.
{% endsi_intro %}

{% si_intro Can I do FPV (first person view) flying with a Crazyflie 2.x? %}
There is ongoing development in this area:

* [Working FPV setup for Crazyflie 2.x](https://forum.bitcraze.io/viewtopic.php?f=6&p=8295).
{% endsi_intro %}



{% si_intro Is it possible to control a swarm of Crazyflies? %}
Yes, it is possible to control multiple Crazyflies simultaneously. It can be done with the Loco Positioning system and our [python library](https://github.com/bitcraze/crazyflie-lib-python/blob/master/examples/swarm/swarmSequence.py) or using [ROS and the ROS driver.](https://wiki.ros.org/crazyflie) For example this video was made using the ROS driver:
[Crazyflie 2.0 Swarm](https://www.youtube.com/watch?v=ezTayb76x9U)
{% endsi_intro %}

{% si_intro Is the Crazyflie 2.0 still supported? %}
Yes, the Crazyflie 2.0 is still supported with the same firmware and PC software as the Crazyflie 2.1
{% endsi_intro %}

{% si_intro Is the Crazyflie 2.x backward compatible with the Crazyflie 1.0 (aka Crazyflie Nano)? %}
No, the Crazyflie 2.x's firmware and python library is no longer backwards compatible, as of the 2017.06 release
{% endsi_intro %}

{% si_intro Is the Crazyflie 1.0 (aka Crazyflie Nano) still supported? %}
No, as of the 2017.06 release of the firmware and PC software, the Crazyflie Nano is no longer supported.
{% endsi_intro %}

<div class="col-md-12">
  <p class="text-right">Want to add a FAQ? <a href="https://github.com/bitcraze/bitcraze-website/edit/master/src/{{page.path}}"><i class="fa-solid fa-pencil"></i> &nbsp;Improve this page</a></p>
</div>

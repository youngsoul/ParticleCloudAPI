Python API to the Particle Cloud API

This ParticleCloud class is meant to be a minimal python implementation
to access a Particle devices (Core, Photon) functions, variables and events.

<b>
    Inspired heavily from:
    
    https://github.com/Alidron/spyrk/blob/master/spyrk/spark_cloud.py
    
    -- Thank you for sharing your implementation
<b>

    ** Create Instance of ParticleCloud
    particle_cloud = ParticleCloud(access_token)
    particle_cloud = ParticleCloud(username, password)

    ** List Devices
    particle_cloud.devices

    ** Call a function
    particle_cloud.internet_button1.ledOn('led1')

    ** Get a variable value
    particle_cloud.internet_button1.buttonCount

    ** Subscribe for a device specific event.
    def callback(event_data):
         print("event callback")

    particle_cloud.internet_button1.subscribe("button1", callback)

    ** Subscribe for a non-device specific event
    particle_cloud.internet_button1.cloud_subscribe("button2", callback)

    ** Publish an event to the cloud
    particle_cloud.internet_button1.publish("do_rainbow")

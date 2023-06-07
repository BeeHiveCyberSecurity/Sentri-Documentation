# ⚙ Configuration

### Before starting <a href="#before-starting" id="before-starting"></a>

Think a little about how your community is structured:

* Which category of roles (users) rarely cause problems?
* Which is the role or group of roles that you _really_ trust? Users who could even help you moderate for brief amounts of time?&#x20;

The answer to these questions will be important during configuration.\
The modules with the most severe effects should, ideally, not affect your highest rank.

{% hint style="warning" %}
Setting core admin and mod roles is **mandatory**. You will not be able to enable Defender until you set them. See the core `[p]set` command.
{% endhint %}



{% hint style="success" %}
Creating a ad-hoc channel for Defender notifications is recommended!&#x20;
{% endhint %}

While Defender takes precautions to ensure that the channel will not be spammed by notifications, it can get intense at times. Plus, having a separate channel allows your staff to better set up their Discord notifications.

### What to do <a href="#what-to-do" id="what-to-do"></a>

{% hint style="danger" %}
It's of paramount importance that you understand how Ranks work before configuring Defender. As a general rule, you may want most if not all of the modules to **only target Rank 2 or below.**
{% endhint %}

Consider the command `[p]def status` your central control panel for all things Defender.

\
From there you can see its overall status plus the status _and_ settings of each module.\
It also serves as your guide when you set things up, as at the bottom of each separate page it will show you which subgroup of commands (in `[p]dset`) to further explore.

As mentioned in the Introduction page, you can choose which functionalities you want to be active. In order to get things up and running, you have to decide which modules you want to use, set them up and toggle them on.

Once you've done that (and fixed any general misconfiguration issue), you are ready to turn on Defender as a whole from the `[p]dset general` subgroup.

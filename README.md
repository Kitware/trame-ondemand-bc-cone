# Batch Connect - Example Trame Application

An example Batch Connect app that launches a Trame Application within a batch job.

# Setup

## Docker Example Cluster

This provides some basic instructions for getting a Docker example cluster
running. If you are running this on a real cluster, skip this section.

1. Clone the repository at https://github.com/ubccr/hpc-toolset-tutorial
2. Run `./hpcts start` inside the repository
3. Go to https://localhost:3443
4. Sign in with username `hpcadmin` and password `ilovelinux`

You should now be in the Open OnDemand Dashboard.

## Real Cluster

If you are running on a real cluster, you will need to change the cluster
name in the `form.yml` file.

You should also install the trame application on the cluster manually
in a virtual environment, and edit the `template/script.sh.erb`
file to activate this virtual environment rather than installing the
`requirements.txt` file.

## Running the Application

1. From the Open OnDemand Dashboard, click "Develop"->"My Sandbox Apps (Development)" from the top menu bar (if you don't see this, please see [this page](https://osc.github.io/ood-documentation/master/app-development/enabling-development-mode.html)).
2. Click "New App", then "Clone Existing App". Put in "trame-example" for the "Directory Name", and then "https://github.com/kitware/trame-ondemand-bc-cone" for the "Git remote". Click "Submit".
3. Click the "Launch Trame App" button on this page or go to "Develop"->"My Sandbox Apps (Development)" and click it from there.
4. Enter relevant settings (for the docker example cluster, you do not need to modify anything - leave "Account" and "Partition" blank). Then click "Launch".
5. Wait until the example trame application is running (for the docker example cluster, it may take ~15 seconds or so to first install the example trame application). Then click the "Connect to Trame App" button.
6. You should be able to see the Trame cone example and interact with it!

![Screenshot from 2022-11-09 16-30-11](https://user-images.githubusercontent.com/9558430/200946781-6ba6f6a8-78c0-418a-9e98-4c2f93e8c02f.png)

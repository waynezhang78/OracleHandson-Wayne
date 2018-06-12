.. Adding labels to the beginning of your lab is helpful for linking to the lab from other pages
.. _example_lab_1:

-------------
Lab 1: Using Swingbench for Oracle Performance Test
-------------

Create Testing Schema
++++++++

Swingbench is a 3rd party tools for testing Oracle database performance . It can provide OLTP or OLAP testing . You can download the swingbench http://dominicgiles.com/swingbench.html
Why we use this tool for the partner training , because the configuration of this tool are vary easy for someone who even no any Oracle experience
There are two job when we using Swingbench testing OLTP performance. First job, you need to create Schema (collection of testing tables and indexes ) .
Create the schema
Go to **/home/oracle/swingbemch/bin** , execute the **./oewizard** to build your schema.

.. figure:: images/createschema.png

The you will see the screen like below , click **Next**

.. figure:: images/OE1.png

Choose Version 2.0 and click **Next**

.. figure:: images/OE2.png

select the **“Create the Order Entry Schema“** and click **“Next”**

.. figure:: images/OE3.png

Change the connect String to **//Hostname/SID** (Depends on your Oracle environment) in this lab is //Linux666/orcl , and the DBA password is qaz12345 (Depends on you Oracle environment), Click **Next**

.. figure:: images/OE4.png

Leave all column default , just in the **Tablespace’s Datafile** input **+DATA** (Your ASM disk group name) as below show, Click **Next**

.. figure:: images/OE5.png

Leave the Database Options don’t change . Click **Next**

.. figure:: images/OE6.png

Change the size as **“10GB”**, it will create about 32GB data in this schema , Click **“Next”**

.. figure:: images/OE7.png

Leave default and Click “Finish”

.. figure:: images/OE8.png

Schema is creating in progress

.. figure:: images/OE9.png

Then you should see the **Schema Created** screen, the invalid should be **None**  , then click **OK** .Then your schema is done.

.. figure:: images/OE10.png

Running Swingbench testing
++++++++++++++++++++++++++

Go to **/home/oracle/swingbemch/bin** , execute the **./swingbench** to run OLTP testing

.. figure:: images/SW1.png

change the **Connect String** to /Linux666/orcl, Linux666 is hostname , orcl is instance name of Oracle (Adjust by your own environment)

.. figure:: images/SW2.png

The click the connection test button **“the blue earth”**, testing swingbench client can be successful connect to Database

.. figure:: images/SW3.png

change the Number of user to 350 , Benchmark Run Tim to 10 minutes and Record Statistic After 5 minutes

.. figure:: images/SW4.png

Click the **Distributed Controls** tab, and type the Hostname to Linux666 , username use root , and Password is qaz12345. After input , please try **“Test Connection”**


.. figure:: images/SW5.png


.. figure:: images/SW6.png

After all set , please click the **Play** the green button.

.. figure:: images/SW7.png

The you can see swingbench start perform OLTP testing .


.. figure:: images/SW8.png

Tutorial of FLINT Reporting tool.
====================================

Introduction
--------------
**FLINT Reporting tool** is a web application that is built on is built on Spring framework Spring Boot, Angular, PostgreSQL, Docker, BASH technologies.
that allows users to configure and manage the reports that are generated by FLINT.
The reports can be of type tables, graphs and some other artifacts, Current version the FLINT Reporting tool generating only 
the **CRF** Tables. 

Structure:
-----------------
The Below diagram shows the flows of execution of the input and the output of the FLINT Reporting Tool.

.. image:: Fourth.png
  :width: 400
  :alt: Alternative text
Mechanics:
----------
Let's understand what exactly does the Reporting tool take in and what does it return.
* **input**
The Input for the FLINT Reporting tool is the FLUX FACT database that is generated by the FLINT, that is
marked by the pools, Date, type and the location. 

**Structure of the Input**:

.. image:: Fifith.png
  :width: 400
  :alt: Alternative text

* The **pools** contains the information where did the material move from and to.
* The **Type** contains the type of the material that was moved.
* The **Date** contains the date of the movement and the location contains the location of the material.
* The **location** contains the information, where the flux occured. The History of the vegetation is stored in the location.

Refer to the below document to understand the pools and FLUX
 `https://docs.moja.global/en/latest/Understanding-FLINT/moja-flint/operations.html#:~:text=The%20amount%20of%20stock%20moved,into%20and%20out%20of%20pools.`

Processing
-------------
* **Processing 1:** Producing land use class history on the basis of the Decision Tree.
* **Processing 2:** It checks the land use,it looks the flux that occured and make the decision where the flux will be aggreated.
* **Processing 3:** FLUX Fact Aggregation Rules.

.. image:: First.png
  :width: 400
  :alt: Processing Final process

Output:
-----------
After the processing the FLINT Reporting tool generates the CRF Tables.

Project Structure:
-------------------
.. note::
    I will write about about the project structure in the next section in proposed timeline.

.. image:: six.png
  :width: 400
  :alt: Processing Final process
Next Steps
-----------
 I will write about the next steps in the proposed timeline.
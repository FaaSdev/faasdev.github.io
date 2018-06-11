===================
Introduction
===================

Concepts
------------

.. Note::

    This part will roughly introduce some concepts related to FaaS since they will help you better understand this
    project and the motivations behind it. 


Serverless Computing
^^^^^^^^^^^^^^^^^^^^

Cloud computing is popularized since Amazon released its EC2 in 2006. The past few years 
have seen the rapid developments of cloud computing, the models of cloud computing have 
changed both in its architectures and its orientation. The most recent hot topics raised 
from this field is widely-known **Serverless Computing**. Such a name makes this model 
a little ambiguous for the general public and the latest architecture **FaaS** is also 
little known to the public. However, more and more people are using these servers either 
consciously or unconsciously. They break through the wall of local computing and support 
more powerful online services such as online language translation, navigation, and so on.

Function as a Service
^^^^^^^^^^^^^^^^^^^^^

Function as a service (FaaS) is a category of cloud computing services that provides a 
platform allowing customers to develop, run, and manage application functionalities 
without the complexity of building and maintaining the infrastructure typically associated 
with developing and launching an app. Building an application following this model is one 
way of achieving a "serverless" architecture, and is typically used when building microservices 
applications. 

API Gateway
^^^^^^^^^^^

**API Gateway** typically works as a set of modules and filters which treat the traffic as it 
flows through it at high speed and you can typically enable those modules / filters you need 
and control their parameters. There are obviously quite a few different ways to actually do 
the implementation + various vendors and open source systems to choose from.(Stackoverflow_)

.. _Stackoverflow: https://stackoverflow.com/questions/11331386/how-do-api-gateways-work

Advantages
----------

- Lower cost: save infrastructure costs, personnel cost, and development costs
- Strong scalability
- Simplied management
- High resource utilization

Motivation
----------

Our project is motivated by Stone_ with his great idea. The original idea is to balance a load 
of servers using FaaS, for some interesting things sharing through WeChat Moments with some 
short period computing needed.

The big problem of such case is not the computation of a single request but a large number of 
requests happened concurrently.

.. _Stone: https://cloud.tencent.com/developer/user/561187/activities
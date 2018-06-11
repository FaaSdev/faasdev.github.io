============
Architecture
============

Description
------------

Our project is based on `Tencent Cloud`_. Three products are used in our project.

.. _`Tencent Cloud`: https://cloud.tencent.com

- SCF_: provide a runtime environmemt. 
- COS_: store staff.
- `API Gateway`_: expose services to users.
 
.. _SCF: https://cloud.tencent.com/product/scf
.. _COS: https://cloud.tencent.com/product/cos
.. _API Gateway: https://cloud.tencent.com/product/apigateway?idx=2


Workflow
---------

APIs is the only service expose to user, which they can directly access. API-gateway 
receive all external user web request and response corresponding processed data. The 
request will be passed to COS or SCF for further handling. COS processes the data 
storage task. SCF deals with image processing.

A whole image processing request contains 4 sub-queries.

1. Get authorized secret key to upload image
    For safety reasons, the user cannot get the authorization for uploading image as 
    the administrator. Users’ image will be checked and users will be returned an 
    authorized signature for uploading an image to COS.
2. Upload image with signature
    User upload image with the signature.
3. Post parameter to image processing
    User post the image processing query to the API, which includes the parameters. 
    A processed image path will be returned.
4. Download processed image 
    User can preview or download processed image from previous path.

.. image:: ./images/architecture.png
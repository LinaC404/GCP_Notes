**I will organize the article later**
<h2>Blue-green deployments</h2>

1. Feature: No downtime and are less risky
1. Process

   - Request->APP1

   - Deploy APP2

   - Request ->APP2

   - Test ... -> OK -> Delete the instances of APP1

<h2>Rolling update</h2>

1. Feature: Compare with blue/green deployment, it can save resources.
1. Process

      NEW VERSION&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;OLD VERSION
   
    |---20% update---->-----------------------------------------------------------------------|

    |--------------40% update------------>----------------------------------------------------|

    |-------------------------60% update--------------------->--------------------------------|

    |-----------------------------------80% update--------------------------->----------------|

    |-------------------------------------------**OK**--------------------------------------------->|

<h2>Canary deployments</h2>

1. Feature: It is similar to blue/green deployment, but more risk-averse.
1. Process

    The version was switched in stages instead of all at once.

    Some users continue to use V1 and some start to use New Version. 

    If no problem happens in New Version, then gradually expand the scope and migrate all users to it.

    &emsp; &emsp; *LoadBalancer*

    V1 V1 V1 V1 NewVersion

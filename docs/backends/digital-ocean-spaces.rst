Digital Ocean
=============

Digital Ocean Spaces implements the S3 protocol. To use it follow the instructions in the :doc:`Amazon S3 docs <amazon-S3>` with the important caveats that you must:

- Set ``AWS_S3_REGION_NAME`` to your Digital Ocean region (such as ``nyc3`` or ``sfo2``)
- Set ``AWS_S3_ENDPOINT_URL`` to the value of ``https://${AWS_S3_REGION_NAME}.digitaloceanspaces.com``
- Set the values of ``AWS_ACCESS_KEY_ID`` and ``AWS_SECRET_ACCESS_KEY`` to the corresponding values from Digital Ocean

As files uploaded to a space do not inherit the access control list of their bucket, you might want to set the ACL for the newly uploaded files to public, to make them available for browsers:

- Set ``AWS_DEFAULT_ACL = "public-read"`` to set the ACL for uploaded files to be publicly readable

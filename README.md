[![CircleCI](https://circleci.com/gh/3scale/apicast-private-ip-blacklist-policy.svg?style=svg)](https://circleci.com/gh/3scale/apicast-private-ip-blacklist-policy)

# APIcast Upstream Private IP Blacklist Policy

This policy will blacklist private IP range and prevent connecting to
those IP addresses as upstream server.


## OpenShift

To install this on OpenShift you can use provided template:

```shell
oc new-app -f openshift.yml --param AMP_RELEASE=2.2.0-GA
```

The template creates new ImageStream for images containing this policy.
Then it creates two BuildConfigs: one for building an image to apicast-policy ImageStream
and second one for creating new APIcast image copying just necessary code from that previous image.


# License

MIT

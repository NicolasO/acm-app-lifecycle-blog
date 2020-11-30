# ACM App LifeCycle Blog

Feel free to fork in order to follow the blog post.
# create the channel 
oc --context hub create -f https://raw.githubusercontent.com/NicolasO/acm-app-lifecycle-blog/master/acm-manifests/base/00_channel.yaml

# create the dev env
oc --context hub create -f https://raw.githubusercontent.com/NicolasO/acm-app-lifecycle-blog/master/acm-manifests/reversewords-stage/00_namespace.yaml
oc --context hub create -f https://raw.githubusercontent.com/NicolasO/acm-app-lifecycle-blog/master/acm-manifests/reversewords-stage/01_placement_rule.yaml
oc --context hub create -f https://raw.githubusercontent.com/NicolasO/acm-app-lifecycle-blog/master/acm-manifests/reversewords-stage/02_subscription-dev.yaml
oc --context hub create -f https://raw.githubusercontent.com/NicolasO/acm-app-lifecycle-blog/master/acm-manifests/reversewords-stage/03_application-dev.yaml

# create the prod env
oc --context hub create -f https://raw.githubusercontent.com/NicolasO/acm-app-lifecycle-blog/master/acm-manifests/reversewords-prod/00_namespace.yaml
oc --context hub create -f https://raw.githubusercontent.com/NicolasO/acm-app-lifecycle-blog/master/acm-manifests/reversewords-prod/01_placement_rule.yaml
oc --context hub create -f https://raw.githubusercontent.com/NicolasO/acm-app-lifecycle-blog/master/acm-manifests/reversewords-prod/02_subscription-pro.yaml
oc --context hub create -f https://raw.githubusercontent.com/NicolasO/acm-app-lifecycle-blog/master/acm-manifests/reversewords-prod/03_application-pro.yaml

kubectl apply -f ./D/nginx.yaml


deployment.apps/nginx-deployment created
service/nginx-deployment created

Den HorizontalPodAutoscaler erstellen:
kubectl autoscale deployment nginx-deployment --cpu-percent=50 --min=1 --max=10

horizontalpodautoscaler.autoscaling/nginx-deployment autoscaled


Den Status vom HorizontalPodAutoscaler überprüfen:
kubectl get hpa

NAME               REFERENCE                     TARGETS   MINPODS   MAXPODS   REPLICAS   AGE
nginx-deployment   Deployment/nginx-deployment   0%/50%    1         10        1          7m25s
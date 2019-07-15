# kubernetes-intro

1. Установлена утилита kubectl;
2. Настроен kubectl autocomplete for bash;
3. Установлен minikube v1.2.0;
4. Установлен addon для Kubernetes - Dashboad;
5. Установлена утилита для консольной работы с кластером - k9s;
6. Проведена проверка на прочность работы кластера при удалении всех pod с системными компонентами:
		- coredns и kubernetes-dashboard (аддоны) запуcкаются как Replica Set, при падении kubelet запускает новые;
		- kube-proxy запущен как Daemon Set, обеспечивается запущенность на каждой ноде;
		- etcd, kube-addon-manager, kube-apiserver, kube-controller-manager, kube-scheduler запускает kubelet как Static Pods;
7. Создан Dockerfile, запускающий http сервер на 8000 порту под пользователем с uid 1001 (использован python);
8. Написан манифест web-pod.yaml;
9. Выполнен деплой пода web и init контейнера;
10. Опробован в работе kube-forwarder.

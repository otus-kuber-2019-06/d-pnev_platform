# d-pnev_platform
d-pnev Platform repository
Установлена утилита kubectl;
Настроен kubectl autocomplete for bash;
Установлен minikube v1.2.0;
Установлен addon для Kubernetes - Dashboad;
Установлена утилита для консольной работы с кластером - k9s;
Проведена проверка на прочность работы кластера при удалении всех pod с системными компонентами: - coredns и kubernetes-dashboard (аддоны) запуcкаются как Replica Set, при падении kubelet запускает новые; - kube-proxy запущен как Daemon Set, обеспечивается запущенность на каждой ноде; - etcd, kube-addon-manager, kube-apiserver, kube-controller-manager, kube-scheduler запускает kubelet как Static Pods;
Создан Dockerfile, запускающий http сервер на 8000 порту под пользователем с uid 1001 (использован python);
Написан манифест web-pod.yaml;
Выполнен деплой пода web и init контейнера;
Опробован в работе kube-forwarder.

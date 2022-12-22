# Настройка jenkins-slave в kubernetes
Используеться kubernetes v1.23.9 запущенный в minikube в режиме драйвера docker
`minikube start --driver=docker --cpus=4 --kubernetes-version=v1.23.9`
Jenkins Master необходимо добавить в сеть minikube и прописать статический айпи адрес ибо куб занимает себе 192.168.49.2 и если первым поднимется jenkins то он будет иметь этот адрес и будет конфликт.
При настройке cloud в jenkins необходимо указать айпишник jenkins-master из подсети minikube иначе поды будут подниматься и сразу сваливаться.

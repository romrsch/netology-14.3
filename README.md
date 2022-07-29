# Домашнее задание к занятию "14.3 Карты конфигураций"

## Задача 1: Работа с картами конфигураций через утилиту kubectl в установленном minikube
Выполните приведённые команды в консоли. Получите вывод команд. Сохраните
задачу 1 как справочный материал.

### Как создать карту конфигураций?
```
kubectl create configmap nginx-config --from-file=nginx.conf
kubectl create configmap domain --from-literal=name=netology.ru
```
***Ответ:***

![Alt test](https://i.ibb.co/T4s7mQ5/Screenshot-1.jpg)

### Как просмотреть список карт конфигураций?
```
kubectl get configmaps
kubectl get configmap
```
***Ответ:***

![Alt text](https://i.ibb.co/VwZkNTm/Screenshot-3.jpg)

### Как просмотреть карту конфигурации?

```
kubectl get configmap nginx-config
kubectl describe configmap domain
```
***Ответ:***

![Alt text](https://i.ibb.co/YRR9gy1/Screenshot-17.jpg)
![Alt text](https://i.ibb.co/DRtQzbD/Screenshot-7.jpg)
![Alt text](https://i.ibb.co/MSZXM5x/Screenshot-6.jpg)

### Как получить информацию в формате YAML и/или JSON?
```
kubectl get configmap nginx-config -o yaml
kubectl get configmap domain -o json
```
***Ответ:***

![Alt text](https://i.ibb.co/wCCH6Wv/Screenshot-12.jpg)
![Alt text](https://i.ibb.co/8BcGgGR/Screenshot-13.jpg)

### Как выгрузить карту конфигурации и сохранить его в файл?
```
kubectl get configmaps -o json > configmaps.json
kubectl get configmap nginx-config -o yaml > nginx-config.yml
```
***Ответ:***

![Alt text](https://i.ibb.co/rFHTCwy/Screenshot-11.jpg)

### Как удалить карту конфигурации?
```
kubectl delete configmap nginx-config
```
***Ответ:***

![Alt text](https://i.ibb.co/3s5Z7w4/Screenshot-15.jpg)

### Как загрузить карту конфигурации из файла?
```
kubectl apply -f nginx-config.yml
```
***Ответ:***

![Alt text](https://i.ibb.co/FwpLGPF/Screenshot-16.jpg)

---

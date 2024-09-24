Перед запуском необходимо изменить параметры хостов следующим образом:
```
    sudo echo 'vm.max_map_count = 262144' >> /etc/sysctl.conf
    sudo sysctl --system
```
Создать CNAME для kibana.local, указывающий на ноды кластера, либо внести изменения в /etc/hosts.

В проекте используется nginx-ingress с ingressClassName: nginx

Развертывание приложения выполняется командой
```
    kubectl apply -f ./deploy
```

Веб-интерфейс приложения доступен по адресу: [http://kibana.local](http://kibana.local)

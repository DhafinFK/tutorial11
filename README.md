# Tutorial 11 - Reflections

## Hello MiniKube tutorial

### 1. Compare the application logs before and after you exposed it as a Service. Try to open the app several times while the proxy into the Service is running. What do you see in the logs? Does the number of logs increase each time you open the app?

Terdapat perbedaan setelah dijadikan service dimana pada address dan port sesuai device kita, aplikasi bisa menerima request beberapa kali. Request-request tersebut dicatat dalam log service hello-node:

![alt text](logs_after_service.png)

### 2. Notice that there are two versions of `kubectl get` invocation during this tutorial section. The first does not have any option, while the latter has `-n` option with value set to `kube-system`. What is the purpose of the `-n` option and why did the output not list the pods/services that you explicitly created?

Penggunaan -n ini menyatakan bahwa service yang kita ingin gunakan berada pada namespace tersebut. Misalnya kita memiliki banyak service berbeda yang punya nama yanmg sama dan tersebar di banyak namespace maka argumen -n ini mengerucutkan untuk mendapatkannya dari namespace yang diberikan setelah -n.
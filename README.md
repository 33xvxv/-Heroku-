【金山文档】 申请Freenom域名的正确做法 https://kdocs.cn/l/cmqB5kYnODzN

【金山文档】 CloudFlare Workers 被墙解决方案 https://kdocs.cn/l/cp7ppdbff6Yw

【金山文档】 Heroku搭建教程 https://kdocs.cn/l/cuGOXoYA2DwO

(https://www.herokucdn.com/deploy/button.png)]https://dashboard.heroku.com/new?template=

CloudFlare Workers 反代代码


addEventListener(
    "fetch",event => {
        let url=new URL(event.request.url);
        url.hostname="输入你注册的应用网址";
        let request=new Request(url,event.request);
        event. respondWith(
            fetch(request)
        )
    }
)

V2rayN 配置如下


- name: "yourName"
    type: vmess
    server: yourName.workers.dev
    port: 443
    uuid: yourUuid
    alterId: 0
    cipher: auto
    udp: true
    tls: true
    #skip-cert-verify: true
    servername: yourName.workers.dev
    network: ws
    ws-path: /


特别鸣谢：Misaka、rptec大佬提供教程和思路



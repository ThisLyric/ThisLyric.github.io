---
layout: post
title: "[ROOT] Security Patch Sideload 보안 패치 올리는 법"
comments: true
categories : [Android/ROOT]
tags: [Android]
---

기본적으로 adb, fastboot는 컴퓨터에

twrp.zip, magisk.zip은 핸드폰 안에 들어가 있는 전제

밑의 링크 들어가서 올리고싶은 버전으로 올리기.

OTA file 다운로드

TWRP 같은 버전 img파일 받아서 platform-tools 폴더 안에 넣어놓기

(편하게 OTA 파일은 update.zip

TWRP 이미지 파일은 twrp.img로

바꾸고 실행)

(MAC은 커맨드 앞에 항상 ./)

```
adb reboot recovery
```

패턴 걸려있으면 풀어주고

Advanced -> ADB Sideload

Swipe to Start Sideload

adb sideload update.zip

Sideload 완료 후에 폰 부팅해 보면 루팅이 풀린 것을 볼 수 있다.

다시 한번 
```
adb reboot recovery
```
부팅하면 기본 리커버리가 실행되므로
```
adb reboot bootloader
```
```
fastboot boot twrp.img
```
twrp 들어간 후에 예전부터 들어가 있던 magisk.zip과 twrp.zip

flash해주면 다시 재루팅 완료




Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

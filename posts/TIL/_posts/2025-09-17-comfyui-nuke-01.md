---
layout: single
title: "[ComfyUI & VFX] Nuke에서 ComfyUI&AI 를 활용하기 01"
tags: ["TIL", "ComfyUI", "VFX", "Nuke", "AI"]
date: "2025-09-17 09:00:00 +0900"
---

> Nuke 에 ComfyUI 초기 & 기즈모 셋팅 (OS:Window)

ComfyUI AI를 Nuke(VFX Comp workflow)에 적용하여 효율을 증대 시킬수 있는가 ? Yes.

먼저 ComfyUI 서버를 사용하여 ComfyUI 노드를 사용할 수 있는 API를 셋팅해야한다.

## 1. ComftUI for Nuke install
1. `.nuke` 폴더에 git clone 
```
git clone --recursive https://github.com/vinavfx/ComfyUI-for-Nuke comfyui2nuke
```

2. Nuke 파이썬 라이브러리에 `websocket-client` 설치 (관리자모드)
```
"C:\Program Files\Nuke15.0v4\python.exe" -m  pip install websocket-client
```

3. `menu.py` 에 코드 추가
```
import comfyui2nuke as comfyui
comfyui.setup()
```

4. `.nuke/comfyui2nuke`의 `settings.py` 환경 잡아주기
- ComfyUI 만 수정하였다.

```
COMFYUI_DIR = os.getenv('NUKE_COMFYUI_DIR', 'D:\ComfyUI')
```


## 2. ComfyUI Gizmos for Nuke install
1. `.nuke\nuke_comfyui\nodes` 폴더에 기즈모 clone 
```
git clone https://github.com/vinavfx/ComfyUI-Gizmos-for-Nuke Gizmos

```

2. Nuke 를 실행하여 ComfyUI 기즈모 확인

![comfyui_nuke_01](/assets/images/comfyui_nuke_01.png)


---
*Reference*

- ComfyUI for Nuke URL : <https://github.com/vinavfx/ComfyUI-for-Nuke>
  - API to be able to use ComfyUI nodes within nuke, only using the ComfyUI server 

- ComfyUI Gizmo for Nuke URL: <https://github.com/vinavfx/ComfyUI-Gizmos-for-Nuke>

- <https://www.alexanderrichtertd.com/post/comfyui-in-nuke-td-meetup>
---
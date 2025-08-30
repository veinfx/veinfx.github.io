---
layout: single
title: "[Jekyll] 작성한 Post가 보이지 않는 Issue"
tags: ["TIL", "git", "Jekyll", "issue"]
date: "2025-08-28 11:30:00 +0900"
---

## Post 를 작성 하였는데 안보임.


### 1. .md post 파일 네이밍 이슈
- 2025-08-29-post.md 처럼 정해진 양식의 파일 이름으로 수정해야한다.

### 2. 해당 index.html Layout 설정 이슈
- `/TIL/index.html` 에서 카테고리와 taxonmy 으로 해당 카테고리를 타겟하도록 잡아야한다.

```
---
layout: category
taxonomy: TIL
title: Today I Learned
---
```

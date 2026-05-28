---
title: 'Projects'
date: 2024-05-19
type: landing

# Page sections
sections:
  - block: collection
    content:
      title: Selected Publication  # 💡 타이틀을 상황에 맞게 변경
      text: Here is the primary research publication highlighting my work.
      filters:
        folders:
          - publications  # 💡 조사 대상을 projects에서 publications 폴더로 변경!
        # featured_only: true  # 💡 오직 '대표작(Featured)'으로 설정된 파일 1개만 불러옵니다.
    design:
      view: article-grid
      fill_image: false
      columns: 1  # 💡 어차피 1개만 나올 거니 시원하게 1열 레이아웃으로 변경
      show_date: true
      show_read_time: false
      show_read_more: false
---
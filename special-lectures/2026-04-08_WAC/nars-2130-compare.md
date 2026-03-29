---
title: "자립준비청년의 자살: 발표용 비교 화면"
layout: default
parent: "이슈페이퍼 작성_사회복지학 신입생 세미나 강좌 WAC 특강(2026.4.8)"
nav_order: 6
permalink: "/special-lectures/2026-04-08/references/nars-2130-compare"
---

<style>
  .compare-stage {
    --compare-ink: #2d2a26;
    --compare-subtle: #5f584f;
    --compare-line: #d7cabb;
    --compare-bg: #f7f1e8;
    color: var(--compare-ink);
  }

  .compare-stage .toolbar {
    position: sticky;
    top: 0;
    z-index: 20;
    display: flex;
    flex-wrap: wrap;
    gap: 0.75rem;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 1rem;
    padding: 0.9rem 1rem;
    border: 1px solid var(--compare-line);
    border-radius: 18px;
    background: rgba(255, 252, 247, 0.95);
    backdrop-filter: blur(8px);
  }

  .compare-stage .toolbar p {
    margin: 0;
    color: var(--compare-subtle);
  }

  .compare-stage .toolbar-links {
    display: flex;
    flex-wrap: wrap;
    gap: 0.6rem;
  }

  .compare-stage .toolbar a {
    display: inline-block;
    padding: 0.55rem 0.85rem;
    border-radius: 999px;
    background: #7c4f2a;
    color: #fff;
    text-decoration: none;
    font-size: 0.95rem;
    font-weight: 700;
  }

  .compare-stage .frame-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
  }

  .compare-stage .frame-card {
    border: 1px solid var(--compare-line);
    border-radius: 20px;
    overflow: hidden;
    background: #fff;
    box-shadow: 0 12px 28px rgba(60, 40, 22, 0.06);
  }

  .compare-stage .frame-card .head {
    padding: 0.85rem 1rem;
    background: var(--compare-bg);
    border-bottom: 1px solid var(--compare-line);
    font-weight: 700;
  }

  .compare-stage iframe {
    display: block;
    width: 100%;
    height: 78vh;
    border: 0;
    background: #fff;
  }

  @media (max-width: 960px) {
    .compare-stage .frame-grid {
      grid-template-columns: 1fr;
    }

    .compare-stage iframe {
      height: 52vh;
    }
  }
</style>

<div class="compare-stage">
  <div class="toolbar">
    <p>발표용 비교 화면입니다. 한 페이지 안에서 원본 재구성본과 대조판을 좌우로 함께 볼 수 있습니다.</p>
    <div class="toolbar-links">
      <a href="/special-lectures/2026-04-08">강의안</a>
      <a href="/special-lectures/2026-04-08/references/nars-2130-original-reconstructed">원본만 보기</a>
      <a href="/special-lectures/2026-04-08/references/nars-2130-original-vs-revised">대조판만 보기</a>
    </div>
  </div>

  <div class="frame-grid">
    <section class="frame-card">
      <div class="head">원본 재구성본</div>
      <iframe src="/special-lectures/2026-04-08/references/nars-2130-original-reconstructed" title="자립준비청년의 자살 원본 재구성본"></iframe>
    </section>
    <section class="frame-card">
      <div class="head">원본-수정안 대조판</div>
      <iframe src="/special-lectures/2026-04-08/references/nars-2130-original-vs-revised" title="자립준비청년의 자살 원본 수정안 대조판"></iframe>
    </section>
  </div>
</div>

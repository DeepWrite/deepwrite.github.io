---
title: 학생 제출용 MD 작성기
layout: default
nav_order: 2
parent: 이슈페이퍼 작성_사회복지학 신입생 세미나 강좌 WAC 특강(2026.4.8)
---

<style>
  .student-writer {
    --writer-ink: #2e2a25;
    --writer-muted: #5b554d;
    --writer-line: #d9cfbf;
    --writer-soft: #f8f3eb;
    --writer-accent: #8b4e1f;
    --writer-accent-strong: #5a3114;
    color: var(--writer-ink);
  }

  .student-writer .hero {
    margin: 1.25rem 0 1.75rem;
    padding: 1.8rem;
    border: 1px solid #dcc8b0;
    border-radius: 24px;
    background:
      radial-gradient(circle at top right, rgba(139, 78, 31, 0.15), transparent 28%),
      linear-gradient(135deg, #fffaf4 0%, #f4e7d6 100%);
    box-shadow: 0 18px 40px rgba(61, 38, 20, 0.06);
  }

  .student-writer .eyebrow {
    display: inline-block;
    margin-bottom: 0.8rem;
    padding: 0.25rem 0.7rem;
    border-radius: 999px;
    background: rgba(139, 78, 31, 0.1);
    color: var(--writer-accent);
    font-size: 0.82rem;
    font-weight: 700;
    letter-spacing: 0.06em;
    text-transform: uppercase;
  }

  .student-writer h1,
  .student-writer h2,
  .student-writer h3,
  .student-writer label,
  .student-writer strong {
    color: var(--writer-accent-strong);
  }

  .student-writer .hero p,
  .student-writer .helper,
  .student-writer .muted {
    color: var(--writer-muted);
  }

  .student-writer .meta-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 1rem;
    margin: 1.25rem 0;
  }

  .student-writer .meta-card,
  .student-writer .panel {
    border: 1px solid var(--writer-line);
    border-radius: 20px;
    background: #fffdfa;
    box-shadow: 0 10px 28px rgba(61, 38, 20, 0.04);
  }

  .student-writer .meta-card {
    padding: 1rem 1.05rem;
  }

  .student-writer .app {
    display: grid;
    grid-template-columns: minmax(280px, 360px) minmax(0, 1fr);
    gap: 1.25rem;
    align-items: start;
  }

  .student-writer .panel {
    padding: 1.1rem;
  }

  .student-writer .panel h2 {
    margin-top: 0;
    margin-bottom: 0.7rem;
    font-size: 1.2rem;
  }

  .student-writer .field {
    margin-bottom: 0.95rem;
  }

  .student-writer label {
    display: block;
    margin-bottom: 0.35rem;
    font-weight: 700;
  }

  .student-writer input,
  .student-writer textarea,
  .student-writer select {
    width: 100%;
    padding: 0.72rem 0.82rem;
    border: 1px solid #cdbfae;
    border-radius: 14px;
    background: #fff;
    color: var(--writer-ink);
    font: inherit;
    box-sizing: border-box;
  }

  .student-writer textarea {
    min-height: 24rem;
    resize: vertical;
    line-height: 1.7;
  }

  .student-writer .tool-row {
    display: flex;
    flex-wrap: wrap;
    gap: 0.55rem;
    margin: 0.9rem 0;
  }

  .student-writer button,
  .student-writer .button-like {
    appearance: none;
    border: 1px solid #bf9d7d;
    border-radius: 999px;
    background: #fff6ee;
    color: var(--writer-accent-strong);
    padding: 0.58rem 0.9rem;
    font: inherit;
    font-weight: 700;
    cursor: pointer;
  }

  .student-writer button.primary {
    background: linear-gradient(135deg, #8b4e1f 0%, #b96d30 100%);
    border-color: #8b4e1f;
    color: #fff;
  }

  .student-writer .generated {
    margin-top: 1rem;
    padding: 0.9rem 1rem;
    border-radius: 16px;
    border: 1px dashed #c8b39c;
    background: var(--writer-soft);
  }

  .student-writer .generated code {
    word-break: break-all;
  }

  .student-writer .preview-box {
    min-height: 10rem;
    white-space: pre-wrap;
    word-break: break-word;
    font-family: ui-monospace, SFMono-Regular, Menlo, Consolas, monospace;
    font-size: 0.93rem;
  }

  .student-writer .note {
    margin-top: 1rem;
    padding: 1rem 1.05rem;
    border-radius: 18px;
    background: #fdf6ee;
    border: 1px solid #e1ccb6;
  }

  @media (max-width: 900px) {
    .student-writer .app {
      grid-template-columns: 1fr;
    }

    .student-writer .hero {
      padding: 1.3rem;
    }
  }
</style>

<div class="student-writer">
  <section class="hero">
    <span class="eyebrow">Student Submission Tool</span>
    <h1>학생 제출용 Markdown 작성기</h1>
    <p>학생이 이름, 학번, 제목, 본문을 입력하면 과제 게시에 바로 쓸 수 있는 <code>.md</code> 파일을 자동 생성해 내려받습니다.</p>

    <div class="meta-grid">
      <div class="meta-card">
        <strong>자동 생성 항목</strong>
        <p class="muted">파일명, YAML front matter, 부모 페이지 연결 정보</p>
      </div>
      <div class="meta-card">
        <strong>도구 버튼</strong>
        <p class="muted">제목 레벨, 굵게, 기울임, 각주 입력 지원</p>
      </div>
      <div class="meta-card">
        <strong>게시 방식</strong>
        <p class="muted">다운로드 후 저장소의 해당 폴더에 올리면 게시 가능</p>
      </div>
    </div>
  </section>

  <div class="app">
    <section class="panel">
      <h2>기본 정보</h2>

      <div class="field">
        <label for="student-name">이름</label>
        <input id="student-name" type="text" placeholder="예: 홍길동">
      </div>

      <div class="field">
        <label for="student-id">학번</label>
        <input id="student-id" type="text" placeholder="예: 20261234">
      </div>

      <div class="field">
        <label for="paper-title">글 제목</label>
        <input id="paper-title" type="text" placeholder="예: 자립준비청년 지원정책의 보완 방향">
      </div>

      <div class="field">
        <label for="slug-fragment">파일명 보조 식별자</label>
        <input id="slug-fragment" type="text" placeholder="비워두면 제목을 기준으로 자동 생성">
        <div class="helper">영문, 숫자, 하이픈 사용을 권장합니다. 예: suicide-policy</div>
      </div>

      <div class="generated">
        <div><strong>생성 파일명</strong></div>
        <code id="filename-preview">2026-04-08-wac-student-paper.md</code>
      </div>

      <div class="generated">
        <div><strong>업로드 권장 경로</strong></div>
        <code>special-lectures/2026-04-08_WAC/</code>
      </div>

      <div class="note">
        <strong>안내</strong>
        <p class="muted">이 작성기는 다운로드용 파일을 만듭니다. 홈페이지에 실제로 게시하려면 내려받은 파일을 저장소에 추가하고 GitHub Pages가 다시 빌드되도록 커밋해야 합니다.</p>
      </div>
    </section>

    <section class="panel">
      <h2>본문 작성</h2>

      <div class="tool-row">
        <button type="button" data-insert="heading-2">H2</button>
        <button type="button" data-insert="heading-3">H3</button>
        <button type="button" data-insert="heading-4">H4</button>
        <button type="button" data-insert="bold">Bold</button>
        <button type="button" data-insert="italic">Italic</button>
        <button type="button" data-insert="footnote">Footnote</button>
      </div>

      <div class="field">
        <label for="paper-body">Markdown 본문</label>
        <textarea id="paper-body" placeholder="# 문제 제기&#10;&#10;이곳에 본문을 작성하세요."></textarea>
      </div>

      <div class="tool-row">
        <button type="button" class="primary" id="download-md">MD 다운로드</button>
        <button type="button" id="copy-frontmatter">YAML 복사</button>
        <button type="button" id="copy-full">전체 문서 복사</button>
      </div>

      <div class="generated">
        <div><strong>자동 생성 YAML 미리보기</strong></div>
        <div id="frontmatter-preview" class="preview-box"></div>
      </div>
    </section>
  </div>
</div>

<script>
  (function () {
    var parentTitle = "이슈페이퍼 작성_사회복지학 신입생 세미나 강좌 WAC 특강(2026.4.8)";
    var writerRoot = "special-lectures/2026-04-08_WAC/";
    var bodyField = document.getElementById("paper-body");
    var nameField = document.getElementById("student-name");
    var idField = document.getElementById("student-id");
    var titleField = document.getElementById("paper-title");
    var slugField = document.getElementById("slug-fragment");
    var filenamePreview = document.getElementById("filename-preview");
    var frontmatterPreview = document.getElementById("frontmatter-preview");

    function escapeYaml(value) {
      return String(value || "").replace(/"/g, '\\"');
    }

    function safeSlug(value) {
      return String(value || "")
        .toLowerCase()
        .trim()
        .replace(/[^a-z0-9가-힣\s-]/g, "")
        .replace(/\s+/g, "-")
        .replace(/-+/g, "-")
        .replace(/^-|-$/g, "");
    }

    function fallbackSlug() {
      var titleSlug = safeSlug(titleField.value);
      var customSlug = safeSlug(slugField.value);
      if (customSlug) return customSlug;
      if (titleSlug) return titleSlug;
      return "paper";
    }

    function currentFilename() {
      var studentId = String(idField.value || "").trim().replace(/[^0-9a-zA-Z_-]/g, "");
      var slug = fallbackSlug();
      var idPart = studentId || "student";
      return "2026-04-08-wac-" + idPart + "-" + slug + ".md";
    }

    function buildFrontmatter() {
      var title = titleField.value.trim() || "제목 미입력";
      var studentName = nameField.value.trim();
      var studentId = idField.value.trim();
      var slug = fallbackSlug();
      var permalink = "/special-lectures/2026-04-08/submissions/" + slug;
      return [
        "---",
        'title: "' + escapeYaml(title) + '"',
        "layout: default",
        'parent: "' + escapeYaml(parentTitle) + '"',
        studentName ? 'author: "' + escapeYaml(studentName) + '"' : 'author: ""',
        studentId ? 'student_id: "' + escapeYaml(studentId) + '"' : 'student_id: ""',
        'permalink: "' + permalink + '"',
        "---"
      ].join("\n");
    }

    function buildDocument() {
      var title = titleField.value.trim() || "제목 미입력";
      var studentName = nameField.value.trim() || "이름 미입력";
      var studentId = idField.value.trim() || "학번 미입력";
      var body = bodyField.value.trim();

      var headerBlock = [
        "# " + title,
        "",
        "- 이름: " + studentName,
        "- 학번: " + studentId,
        ""
      ].join("\n");

      return [
        buildFrontmatter(),
        "",
        headerBlock,
        body
      ].join("\n");
    }

    function refreshPreview() {
      filenamePreview.textContent = currentFilename();
      frontmatterPreview.textContent = buildFrontmatter();
    }

    function insertAroundSelection(prefix, suffix, placeholder) {
      var start = bodyField.selectionStart;
      var end = bodyField.selectionEnd;
      var selected = bodyField.value.slice(start, end) || placeholder;
      var replacement = prefix + selected + suffix;
      bodyField.setRangeText(replacement, start, end, "end");
      bodyField.focus();
      refreshPreview();
    }

    function insertHeading(level) {
      var start = bodyField.selectionStart;
      var end = bodyField.selectionEnd;
      var selected = bodyField.value.slice(start, end) || "제목을 입력하세요";
      var prefix = (start > 0 && bodyField.value.charAt(start - 1) !== "\n") ? "\n" : "";
      var replacement = prefix + level + " " + selected + "\n";
      bodyField.setRangeText(replacement, start, end, "end");
      bodyField.focus();
      refreshPreview();
    }

    function insertFootnote() {
      var body = bodyField.value;
      var matches = body.match(/\[\^(\d+)\]/g);
      var nextNumber = matches ? matches.length + 1 : 1;
      var marker = "[^" + nextNumber + "]";
      var note = "\n\n" + marker + ": 각주 내용을 입력하세요.";
      var start = bodyField.selectionStart;
      var end = bodyField.selectionEnd;
      var selected = bodyField.value.slice(start, end) || "각주가 필요한 문장";
      bodyField.setRangeText(selected + marker + note, start, end, "end");
      bodyField.focus();
      refreshPreview();
    }

    function copyText(text) {
      if (navigator.clipboard && navigator.clipboard.writeText) {
        navigator.clipboard.writeText(text);
      }
    }

    document.querySelectorAll("[data-insert]").forEach(function (button) {
      button.addEventListener("click", function () {
        var action = button.getAttribute("data-insert");
        if (action === "heading-2") insertHeading("##");
        if (action === "heading-3") insertHeading("###");
        if (action === "heading-4") insertHeading("####");
        if (action === "bold") insertAroundSelection("**", "**", "강조할 문장");
        if (action === "italic") insertAroundSelection("*", "*", "기울일 문장");
        if (action === "footnote") insertFootnote();
      });
    });

    document.getElementById("copy-frontmatter").addEventListener("click", function () {
      copyText(buildFrontmatter());
    });

    document.getElementById("copy-full").addEventListener("click", function () {
      copyText(buildDocument());
    });

    document.getElementById("download-md").addEventListener("click", function () {
      var content = buildDocument();
      var blob = new Blob([content], { type: "text/markdown;charset=utf-8" });
      var link = document.createElement("a");
      link.href = URL.createObjectURL(blob);
      link.download = currentFilename();
      document.body.appendChild(link);
      link.click();
      document.body.removeChild(link);
      URL.revokeObjectURL(link.href);
    });

    [nameField, idField, titleField, slugField, bodyField].forEach(function (field) {
      field.addEventListener("input", refreshPreview);
    });

    bodyField.value = [
      "## 문제 제기",
      "",
      "이 글이 다루는 핵심 현안과 그 중요성을 간략히 설명합니다.",
      "",
      "## 쟁점 분석",
      "",
      "서로 다른 입장과 그 근거를 공정하게 정리합니다.",
      "",
      "## 나의 논제",
      "",
      "이 글의 핵심 주장을 한 문장으로 제시합니다.",
      "",
      "## 개선 방향",
      "",
      "실현 가능한 대안을 제안합니다."
    ].join("\n");

    refreshPreview();
  }());
</script>

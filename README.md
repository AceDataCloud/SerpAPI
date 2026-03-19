# Search Engine API

Search Engine Results Page (SERP) related API.

![Platform](https://img.shields.io/badge/platform-Ace%20Data%20Cloud-0f766e?style=flat-square) ![API](https://img.shields.io/badge/type-AI%20API-2563eb?style=flat-square) ![Docs](https://img.shields.io/badge/docs-online-16a34a?style=flat-square)

![Search Engine](https://cdn.acedata.cloud/o5gj5l.png/thumb_600x300)

API home page: [Ace Data Cloud - Search Engine](https://platform.acedata.cloud/service/serp)

Keywords: serp-api, web-search, google-search, search-api, rest-api, ai-api, AI API, REST API, Developer API, Ace Data Cloud

## Why Use Search Engine on Ace Data Cloud

- Unified developer platform with one API key, billing system, and usage tracking
- Production-ready AI API endpoints served from [https://api.acedata.cloud](https://api.acedata.cloud)
- English integration guides, API references, and service documentation
- Global-ready workflow for developers building chat, image, video, music, and search products

## Overview

<style>
.serp-page * { box-sizing: border-box; }
.serp-page h1, .serp-page h2, .serp-page h3, .serp-page h4, .serp-page h5, .serp-page h6, .serp-page p, .serp-page ul, .serp-page ol, .serp-page li, .serp-page pre, .serp-page blockquote, .serp-page table, .serp-page td, .serp-page th { margin: 0; padding: 0; }
.serp-page {
-webkit-font-smoothing: antialiased;
-moz-osx-font-smoothing: grayscale;
color: var(--el-text-color-primary);
background: var(--el-bg-color);
line-height: 1.6;
}
.serp-page a { text-decoration: none; color: inherit; }
.serp-page a:hover { text-decoration: none; }
.serp-page ul { list-style: none; }
.markdown-body .serp-page a { color: inherit !important; text-decoration: none !important; }
.markdown-body .serp-page a:hover { text-decoration: none !important; }
.markdown-body .serp-page a.sp-btn-primary,
.markdown-body .serp-page a.btn-cta-light { color: #ffffff !important; }
.markdown-body .serp-page a.sp-btn-secondary { color: var(--el-text-color-primary) !important; }
.markdown-body .serp-page a.btn-cta-ghost { color: #94a3b8 !important; }
.markdown-body .serp-page a.btn-cta-ghost:hover { color: #e2e8f0 !important; }
.markdown-body .serp-page h1, .markdown-body .serp-page h2 { border-bottom: none !important; padding-bottom: 0 !important; }
.sp-container { max-width: 1200px; margin: 0 auto; padding: 0 24px; }
.sp-container-narrow { max-width: 800px; margin: 0 auto; padding: 0 24px; }
.sp-section { padding: 80px 0; }
.sp-section-sm { padding: 48px 0; }
.sp-bg-white { background: var(--el-bg-color); }
.sp-bg-gray { background: var(--el-bg-color-page); }
.sp-header { text-align: center; margin-bottom: 64px; }
.sp-header h2 {
font-size: clamp(28px, 4vw, 40px);
font-weight: 700;
color: var(--el-text-color-primary);
letter-spacing: normal;
margin-bottom: 20px;
line-height: 1.15;
}
.sp-header p {
font-size: clamp(16px, 2vw, 18px);
color: var(--el-text-color-regular);
max-width: 640px;
margin: 0 auto;
line-height: 1.6;
}
.serp-page .sp-btn-primary {
display: inline-flex; align-items: center; gap: 6px;
padding: 14px 28px;
background: #2563eb; color: #ffffff !important;
border-radius: 9999px; font-size: 15px; font-weight: 600;
transition: background 0.2s, transform 0.15s;
border: none; cursor: pointer;
text-decoration: none !important;
}
.serp-page .sp-btn-primary:hover { background: #1d4ed8; transform: translateY(-1px); text-decoration: none !important; }
.serp-page .sp-btn-secondary {
display: inline-flex; align-items: center; gap: 6px;
padding: 14px 28px;
background: var(--el-bg-color); color: var(--el-text-color-primary) !important;
border: 1px solid var(--el-border-color-light);
border-radius: 9999px; font-size: 15px; font-weight: 600;
transition: border-color 0.2s, background 0.2s;
cursor: pointer;
text-decoration: none !important;
}
.serp-page .sp-btn-secondary:hover { background: var(--el-bg-color-page); text-decoration: none !important; }
.serp-hero {
padding: 100px 0 80px;
text-align: center;
background: var(--el-bg-color);
position: relative;
overflow: hidden;
}
.serp-hero::before {
content: '';
position: absolute;
top: -200px; left: 50%;
transform: translateX(-50%);
width: 900px; height: 500px;
background: radial-gradient(ellipse, rgba(37, 99, 235, 0.06) 0%, transparent 70%);
pointer-events: none;
}
.sp-badge {
display: inline-flex; align-items: center; gap: 8px;
padding: 6px 16px;
background: var(--el-bg-color-page); border: 1px solid var(--el-border-color-light);
border-radius: 9999px; font-size: 13px; font-weight: 600; color: var(--el-text-color-regular);
margin-bottom: 28px;
}
.sp-badge-dot {
width: 6px; height: 6px; background: #10b981; border-radius: 50%;
display: inline-block;
}
.serp-hero h1 {
font-size: clamp(36px, 5vw, 60px);
line-height: 1.08;
letter-spacing: normal;
margin-bottom: 18px;
font-weight: 700;
}
.serp-hero h1 .sp-brand { color: #2563eb; }
.serp-hero h1 .sp-sub { color: var(--el-text-color-primary); }
.serp-page .hero-subtitle {
max-width: 680px;
margin: 0 auto;
font-size: clamp(16px, 2.1vw, 20px);
color: var(--el-text-color-regular);
line-height: 1.6;
}
.sp-actions {
margin-top: 56px;
display: flex; gap: 12px;
justify-content: center;
flex-wrap: wrap;
}
.sp-highlights {
display: flex; gap: 24px; justify-content: center; flex-wrap: wrap;
margin-top: 40px;
}
.sp-highlights .h-item { font-size: 13px; color: var(--el-text-color-regular); display: flex; align-items: center; gap: 6px; }
.sp-highlights .h-div { width: 1px; height: 14px; background: var(--el-border-color-light); }
.sp-stats {
display: grid !important;
grid-template-columns: repeat(4, 1fr) !important;
gap: 20px !important;
}
.sp-stat {
background: var(--el-bg-color);
border: 1px solid var(--el-border-color-light);
border-radius: 16px;
padding: 24px 16px;
text-align: center;
}
.sp-stat-val {
font-size: clamp(28px, 4vw, 38px);
font-weight: 700;
color: var(--el-text-color-primary);
line-height: 1.1;
}
.sp-stat-lbl { margin-top: 8px; font-size: 13px; color: var(--el-text-color-regular); }
.sp-feat-grid {
display: grid !important;
grid-template-columns: repeat(2, 1fr) !important;
gap: 20px !important;
}
.sp-feat-card {
background: var(--el-bg-color);
border: 1px solid var(--el-border-color-light);
border-radius: 16px;
padding: 28px 24px;
transition: border-color 0.2s;
}
.sp-feat-card:hover { border-color: var(--el-text-color-regular); }
.sp-feat-card h3 { font-size: 18px; font-weight: 700; color: var(--el-text-color-primary); margin-bottom: 8px; }
.sp-feat-card p { font-size: 15px; color: var(--el-text-color-regular); line-height: 1.6; }
.sp-feat-icon { font-size: 28px; margin-bottom: 12px; }
.sp-code-wrap {
border-radius: 16px !important;
overflow: hidden !important;
border: 1px solid #334155 !important;
background: #0f172a !important;
}
.markdown-body .serp-page .sp-code-wrap { background: #0f172a !important; }
.sp-code-head {
padding: 10px 16px;
background: #1e293b;
border-bottom: 1px solid #334155;
color: #cbd5e1;
font-size: 12px;
letter-spacing: 0.06em;
text-transform: uppercase;
}
.sp-code
{
margin: 0 !important;
padding: 18px !important;
white-space: pre !important;
overflow-x: auto !important;
font-family: 'JetBrains Mono', 'Fira Code', 'SFMono-Regular', monospace !important;
font-size: 13px !important;
line-height: 1.7 !important;
color: #e2e8f0 !important;
background: transparent !important;
border: none !important;
}
.markdown-body .serp-page .sp-code { background: transparent !important; }
.sp-code-grid {
display: grid !important;
grid-template-columns: 1fr 1fr !important;
gap: 0 !important;
align-items: stretch;
}
.sp-code-left {
display: flex; flex-direction: column; justify-content: center;
padding: 0 40px 0 0;
}
.sp-code-left h2 {
font-size: clamp(24px, 3.2vw, 34px);
font-weight: 700;
color: var(--el-text-color-primary);
margin-bottom: 16px;
}
.sp-code-left > p {
font-size: 16px; color: var(--el-text-color-regular); line-height: 1.6;
}
.sp-steps {
display: grid !important;
grid-template-columns: repeat(3, 1fr) !important;
gap: 0 !important;
position: relative;
}
.sp-step { text-align: center; padding: 0 24px; }
.sp-step-num {
width: 44px; height: 44px;
border-radius: 50%;
background: var(--el-bg-color-page);
border: 2px solid var(--el-border-color-light);
display: inline-flex; align-items: center; justify-content: center;
font-size: 16px; font-weight: 700; color: var(--el-text-color-regular);
margin-bottom: 16px;
}
.sp-step h3 { font-size: 17px; font-weight: 700; color: var(--el-text-color-primary); margin-bottom: 8px; }
.sp-step p { font-size: 14px; color: var(--el-text-color-regular); line-height: 1.6; }
.sp-step-conn {
position: absolute;
top: 22px;
height: 2px;
background: var(--el-border-color-light);
}
.sp-step-conn-1 { left: calc(100% / 6); right: calc(100% / 6 * 3); }
.sp-step-conn-2 { left: calc(100% / 6 * 3); right: calc(100% / 6); }
.sp-uc-grid {
display: grid !important;
grid-template-columns: repeat(3, 1fr) !important;
gap: 20px !important;
}
.sp-uc-card {
background: var(--el-bg-color);
border: 1px solid var(--el-border-color-light);
border-radius: 16px;
padding: 24px;
transition: border-color 0.2s;
}
.sp-uc-card:hover { border-color: var(--el-text-color-regular); }
.sp-uc-icon { font-size: 28px; margin-bottom: 10px; }
.sp-uc-card h3 { font-size: 16px; font-weight: 700; color: var(--el-text-color-primary); margin-bottom: 6px; }
.sp-uc-card p { font-size: 14px; color: var(--el-text-color-regular); line-height: 1.5; }
.sp-param-grid {
display: grid !important;
grid-template-columns: repeat(3, 1fr) !important;
gap: 20px !important;
}
.sp-param-card {
background: var(--el-bg-color);
border: 1px solid var(--el-border-color-light);
border-radius: 16px;
padding: 24px;
}
.sp-param-card h3 { font-size: 16px; font-weight: 700; color: var(--el-text-color-primary); margin-bottom: 4px; }
.serp-page .sp-param-card .param-desc { font-size: 14px; color: var(--el-text-color-regular); line-height: 1.5; }
.sp-param-val {
display: inline-block;
padding: 2px 8px;
background: var(--el-bg-color-page);
border-radius: 6px;
font-size: 12px;
color: var(--el-text-color-regular);
font-family: 'JetBrains Mono', monospace;
margin-bottom: 8px;
}
.sp-price-table-wrap {
max-width: 640px;
margin: 0 auto;
border-radius: 16px;
overflow: hidden;
border: 1px solid var(--el-border-color-light);
}
.sp-price-table {
display: table !important;
width: 100% !important;
border-collapse: collapse !important;
}
.sp-price-table th {
padding: 14px 20px !important;
background: var(--el-bg-color-page) !important;
font-size: 13px !important;
font-weight: 700 !important;
color: var(--el-text-color-regular) !important;
text-transform: uppercase !important;
letter-spacing: 0.06em !important;
text-align: left !important;
border: none !important;
border-bottom: 1px solid var(--el-border-color-light) !important;
}
.sp-price-table td {
padding: 14px 20px !important;
font-size: 15px !important;
color: var(--el-text-color-primary) !important;
border: none !important;
border-bottom: 1px solid var(--el-border-color-lighter) !important;
background: var(--el-bg-color) !important;
}
.sp-price-table tr:last-child td { border-bottom: none !important; }
.sp-price-table .td-price {
color: #2563eb !important;
font-weight: 700 !important;
font-family: 'JetBrains Mono', monospace !important;
}
.sp-price-note {
text-align: center;
font-size: 13px;
color: var(--el-text-color-regular);
margin-top: 16px;
}
.sp-faq-list { max-width: 800px; margin: 0 auto; }
.sp-faq-item { border-bottom: 1px solid var(--el-border-color-lighter); }
.sp-faq-q {
display: flex; justify-content: space-between; align-items: center;
padding: 20px 0; cursor: pointer;
font-size: 16px; font-weight: 600; color: var(--el-text-color-primary);
transition: color 0.2s;
}
.sp-faq-q:hover { color: #2563eb; }
.sp-faq-chev { font-size: 18px; color: var(--el-text-color-regular); transition: transform 0.2s; }
.sp-faq-a { display: none; padding: 0 0 20px; }
.sp-faq-a p { font-size: 15px; color: var(--el-text-color-regular); line-height: 1.7; }
.sp-rel-grid {
display: grid !important;
grid-template-columns: repeat(4, 1fr) !important;
gap: 16px !important;
}
.sp-rel-card {
display: flex; align-items: center; gap: 14px;
background: var(--el-bg-color);
border: 1px solid var(--el-border-color-light);
border-radius: 14px;
padding: 16px 18px;
transition: border-color 0.2s;
}
.sp-rel-card:hover { border-color: var(--el-text-color-regular); }
.sp-rel-icon { font-size: 28px; flex-shrink: 0; }
.sp-rel-info h3 { font-size: 15px; font-weight: 700; color: var(--el-text-color-primary); }
.sp-rel-info p { font-size: 12px; color: var(--el-text-color-regular); margin-top: 2px; }
.sp-rel-arrow { margin-left: auto; font-size: 16px; color: var(--el-border-color); transition: color 0.2s; }
.sp-rel-card:hover .sp-rel-arrow { color: var(--el-text-color-regular); }
.serp-cta {
text-align: center;
background: #0f172a;
color: #f8fafc;
padding: 80px 0;
position: relative;
overflow: hidden;
}
.serp-cta::before
{
content: '';
position: absolute;
top: -100px; left: 50%;
transform: translateX(-50%);
width: 600px; height: 400px;
background: radial-gradient(ellipse, rgba(37, 99, 235, 0.15) 0%, transparent 70%);
pointer-events: none;
}
.serp-cta h2 {
font-size: clamp(30px, 4.2vw, 46px);
font-weight: 700;
letter-spacing: normal;
margin-bottom: 28px;
position: relative;
}
.serp-cta p {
font-size: 17px;
color: #cbd5e1;
max-width: 600px;
margin: 0 auto 56px;
position: relative;
}
.serp-cta .sp-actions { position: relative; margin-top: 0; }
.serp-page .btn-cta-light {
display: inline-flex; align-items: center; gap: 6px;
padding: 14px 28px;
background: #2563eb; color: #ffffff !important;
border-radius: 9999px; font-size: 15px; font-weight: 600;
transition: background 0.2s;
text-decoration: none !important;
}
.serp-page .btn-cta-light:hover { background: #1d4ed8; }
.serp-page .btn-cta-ghost {
display: inline-flex; align-items: center; gap: 6px;
padding: 14px 28px;
background: transparent; color: #94a3b8 !important;
border: 1px solid #475569;
border-radius: 9999px; font-size: 15px; font-weight: 600;
transition: border-color 0.2s, color 0.2s;
text-decoration: none !important;
}
.serp-page .btn-cta-ghost:hover { border-color: #94a3b8; color: #e2e8f0 !important; }
.serp-page code
{
background: #eff6ff !important; color: #2563eb !important;
border: 1px solid #bfdbfe !important;
padding: 2px 6px !important; border-radius: 4px !important;
font-size: 0.88em !important; font-weight: 600 !important;
}
html.dark .serp-page { background: var(--el-bg-color); color: var(--el-text-color-primary); }
html.dark .markdown-body .serp-page a { color: inherit !important; }
html.dark .markdown-body .serp-page a.sp-btn-primary,
html.dark .markdown-body .serp-page a.btn-cta-light { color: #ffffff !important; }
html.dark .markdown-body .serp-page a.sp-btn-secondary { color: var(--el-text-color-primary) !important; }
html.dark .markdown-body .serp-page a.btn-cta-ghost { color: #94a3b8 !important; }
html.dark .markdown-body .serp-page a.btn-cta-ghost:hover { color: var(--el-text-color-primary) !important; }
html.dark .sp-bg-white { background: var(--el-bg-color); }
html.dark .sp-bg-gray { background: var(--el-bg-color-page); }
html.dark .sp-header h2 { color: var(--el-text-color-primary); }
html.dark .sp-header p { color: var(--el-text-color-secondary); }
html.dark .serp-page .sp-btn-primary { background: #2563eb; }
html.dark .serp-page .sp-btn-primary:hover { background: #1d4ed8; }
html.dark .serp-page .sp-btn-secondary { background: #1e293b; color: var(--el-text-color-primary) !important; border-color: #475569; }
html.dark .serp-page .sp-btn-secondary:hover { background: var(--el-border-color); border-color: var(--el-text-color-regular); }
html.dark .serp-hero { background: var(--el-bg-color); }
html.dark .serp-hero::before { background: radial-gradient(ellipse, rgba(37, 99, 235, 0.15) 0%, transparent 70%); }
html.dark .sp-badge { background: var(--el-bg-color-page); border-color: var(--el-border-color); color: var(--el-text-color-secondary); }
html.dark .serp-hero h1 .sp-brand { color: #60a5fa; }
html.dark .serp-hero h1 .sp-sub { color: var(--el-text-color-primary); }
html.dark .serp-page .hero-subtitle { color: var(--el-text-color-secondary); }
html.dark .sp-highlights .h-item { color: var(--el-text-color-secondary); }
html.dark .sp-highlights .h-div { background: var(--el-border-color); }
html.dark .sp-stat { background: var(--el-bg-color-page); border-color: var(--el-border-color); box-shadow: none; }
html.dark .sp-stat-val { color: var(--el-text-color-primary); }
html.dark .sp-stat-lbl { color: var(--el-text-color-regular); }
html.dark .sp-feat-card { background: var(--el-bg-color-page); border-color: var(--el-border-color); }
html.dark .sp-feat-card:hover { border-color: var(--el-text-color-regular); }
html.dark .sp-feat-card h3 { color: var(--el-text-color-primary); }
html.dark .sp-feat-card p { color: var(--el-text-color-secondary); }
html.dark .sp-code-left h2 { color: var(--el-text-color-primary); }
html.dark .sp-code-left > p { color: var(--el-text-color-secondary); }
html.dark .sp-step-num { background: var(--el-border-color); border-color: var(--el-text-color-regular); color: var(--el-text-color-secondary); }
html.dark .sp-step h3 { color: var(--el-text-color-primary); }
html.dark .sp-step p { color: var(--el-text-color-regular); }
html.dark .sp-step-conn { background: var(--el-border-color); }
html.dark .sp-uc-card { background: var(--el-bg-color-page); border-color: var(--el-border-color); }
html.dark .sp-uc-card:hover { border-color: var(--el-text-color-regular); }
html.dark .sp-uc-card h3 { color: var(--el-text-color-primary); }
html.dark .sp-uc-card p { color: var(--el-text-color-secondary); }
html.dark .sp-param-card { background: var(--el-bg-color-page); border-color: var(--el-border-color); }
html.dark .sp-param-card h3 { color: var(--el-text-color-primary); }
html.dark .serp-page .sp-param-card .param-desc { color: var(--el-text-color-secondary); }
html.dark .sp-param-val { background: var(--el-border-color); color: var(--el-text-color-secondary); }
html.dark .sp-price-table-wrap { border-color: var(--el-border-color); }
html.dark .sp-price-table th { background: var(--el-bg-color-page) !important; color: var(--el-text-color-secondary) !important; border-bottom-color: var(--el-border-color) !important; }
html.dark .sp-price-table td { color: var(--el-text-color-primary) !important; border-bottom-color: var(--el-border-color) !important; background: var(--el-bg-color) !important; }
html.dark .sp-price-table .td-price { color: #60a5fa !important; }
html.dark .sp-price-note { color: var(--el-text-color-secondary); }
html.dark .sp-faq-item { border-color: var(--el-border-color); }
html.dark .sp-faq-q { color: var(--el-text-color-primary); }
html.dark .sp-faq-q:hover { color: #60a5fa; }
html.dark .sp-faq-chev { color: var(--el-text-color-regular); }
html.dark .sp-faq-a p { color: var(--el-text-color-secondary); }
html.dark .sp-rel-card { background: var(--el-bg-color-page); border-color: var(--el-border-color); }
html.dark .sp-rel-card:hover { border-color: var(--el-text-color-regular); }
html.dark .sp-rel-info h3 { color: var(--el-text-color-primary); }
html.dark .sp-rel-info p { color: var(--el-text-color-regular); }
html.dark .sp-rel-arrow { color: var(--el-text-color-regular); }
html.dark .serp-cta { background: #020617; }
html.dark .serp-cta::before { background: radial-gradient(ellipse, rgba(37, 99, 235, 0.2) 0%, transparent 70%); }
html.dark .serp-page .btn-cta-light { color: #ffffff !important; }
html.dark .serp-page .btn-cta-ghost { color: #94a3b8 !important; }
html.dark .serp-page .btn-cta-ghost:hover { color: var(--el-text-color-primary) !important; }
html.dark .serp-page code { background: #1e3a5f !important; color: #93c5fd !important; border-color: #3b82f6 !important; }
@media (max-width: 980px) {
.sp-stats { grid-template-columns: repeat(2, 1fr) !important; }
.sp-feat-grid { grid-template-columns: 1fr !important; }
.sp-code-grid { grid-template-columns: 1fr !important; }
.sp-code-left { padding: 0 0 32px 0; }
.sp-steps { grid-template-columns: 1fr !important; gap: 24px !important; }
.sp-step-conn { display: none; }
.sp-uc-grid { grid-template-columns: 1fr !important; }
.sp-param-grid { grid-template-columns: 1fr !important; }
.sp-rel-grid { grid-template-columns: repeat(2, 1fr) !important; }
}
@media (max-width: 480px) {
.sp-stats { grid-template-columns: 1fr !important; }
.sp-rel-grid { grid-template-columns: 1fr !important; }
}
</style>
<div class="serp-page">
<section class="serp-hero">
<div class="sp-container">
<div class="sp-badge"><span class="sp-badge-dot"></span>Search Engine · Results Page</div>
<h1><span class="sp-brand">SERP</span> <span class="sp-sub">Search Engine API</span></h1>
<p class="hero-subtitle">Get Google search results through a simple RESTful API. Supports web search, image search, news search—charged by the number of requests, starting at $0.00095.</p>
<div class="sp-actions">
<a class="sp-btn-primary" href="/apis/serp-google">📄 View Documentation</a>
<a class="sp-btn-secondary" href="/apis/serp-google">🔍 API Reference</a>
</div>
<div class="sp-highlights">
<span class="h-item">🌐 Google Search</span>
<span class="h-div"></span>
<span class="h-item">🖼️ Image Search</span>
<span class="h-div"></span>
<span class="h-item">📰 News Search</span>
<span class="h-div"></span>
<span class="h-item">💰 $0.00095 / request starting</span>
</div>
</div>
</section>
<section class="sp-section-sm sp-bg-gray">
<div class="sp-container">
<div class="sp-stats">
<div class="sp-stat"><div class="sp-stat-val">$0.00095</div><div class="sp-stat-lbl">Starting price per search</div></div>
<div class="sp-stat"><div class="sp-stat-val">100+</div><div class="sp-stat-lbl">Supported countries/regions</div></div>
<div class="sp-stat"><div class="sp-stat-val">Real-time</div><div class="sp-stat-lbl">Result data</div></div>
<div class="sp-stat"><div class="sp-stat-val">JSON</div><div class="sp-stat-lbl">Structured response</div></div>
</div>
</div>
</section>
<section class="sp-section sp-bg-white">
<div class="sp-container">
<div class="sp-header">
<h2>Core Features</h2>
<p>One API to get all search results from Google Search Engine</p>
</div>
<div class="sp-feat-grid">
<div class="sp-feat-card">
<div class="sp-feat-icon">🌐</div>
<h3>Web Search</h3>
<p>Get Google web search results, including complete information such as title, summary, link, etc., supporting pagination and custom result counts.</p>
</div>
<div class="sp-feat-card">
<div class="sp-feat-icon">🖼️</div>
<h3>Image Search</h3>
<p>Search Google images, returning structured data such as image URLs, thumbnails, and sources for image collection and analysis.</p>
</div>
<div class="sp-feat-card">
<div class="sp-feat-icon">📰</div>
<h3>News Search</h3>
<p>Get Google news results, tracking hot events in real-time, suitable for news aggregation applications.</p>
</div>
<div class="sp-feat-card">
<div class="sp-feat-icon">🌍</div>
<h3>Multilingual and Multiregional</h3>
<p>Specify the country and language for search using <code>gl</code> and <code>hl</code> parameters to get localized search results.</p>
</div>
</div>
</div>
</section>
<section class="sp-section sp-bg-gray">
<div class="sp-container">
<div class="sp-code-grid">
<div class="sp-code-left">
<h2>Get search results in one line of code</h2>
<p>Concise RESTful API design, structured Google search data can be obtained with a GET request.</p>
</div>
<div>
<div class="sp-code-wrap">
<div class="sp-code-head">Python</div>
<pre class="sp-code">import requests
 

response = requests.get(
"https://api.acedata.cloud/serp/google",
headers={
"Authorization": "Bearer YOUR_API_KEY"
},
params={
"q": "artificial intelligence",
"number": 10,
"gl": "us",
"hl": "en"
}
)
```python
data = response.json()
for result in data["results"]:
    print(result["title"], result["link"])
```
</pre>
</div>
</div>
</div>
</div>
</section>
<section class="sp-section sp-bg-white">
<div class="sp-container">
<div class="sp-header">
<h2>3 Steps to Get Started Quickly</h2>
<p>It only takes a few minutes from registration to getting your first search result.</p>
</div>
<div class="sp-steps">
<div class="sp-step-conn sp-step-conn-1"></div>
<div class="sp-step-conn sp-step-conn-2"></div>
<div class="sp-step">
<div class="sp-step-num">1</div>
<h3>Get API Key</h3>
<p>Register and generate an API key from the console.</p>
</div>
<div class="sp-step">
<div class="sp-step-num">2</div>
<h3>Build Search Request</h3>
<p>Set parameters such as keywords, language, number of results, etc.</p>
</div>
<div class="sp-step">
<div class="sp-step-num">3</div>
<h3>Get Results</h3>
<p>Send a GET request to obtain search results in JSON format.</p>
</div>
</div>
</div>
</section>
<section class="sp-section sp-bg-gray">
<div class="sp-container">
<div class="sp-header">
<h2>What is SERP API Suitable For?</h2>
<p>Covers various application scenarios for search engine data</p>
</div>
<div class="sp-uc-grid">
<div class="sp-uc-card">
<div class="sp-uc-icon">📊</div>
<h3>SEO Monitoring</h3>
<p>Track keyword ranking changes and analyze competitors' search performance.</p>
</div>
<div class="sp-uc-card">
<div class="sp-uc-icon">🤖</div>
<h3>AI Agent Tools</h3>
<p>Provide real-time search capabilities for LLM Agents to obtain the latest internet information.</p>
</div>
<div class="sp-uc-card">
<div class="sp-uc-icon">📰</div>
<h3>Public Opinion Monitoring</h3>
<p>Monitor brand-related news and changes in search results in real-time.</p>
</div>
<div class="sp-uc-card">
<div class="sp-uc-icon">📈</div>
<h3>Market Research</h3>
<p>Bulk obtain industry-related search data to assist in market analysis decisions.</p>
</div>
<div class="sp-uc-card">
<div class="sp-uc-icon">🔬</div>
<h3>Academic Research</h3>
<p>Large-scale search data collection for academic research and paper writing.</p>
</div>
<div class="sp-uc-card">
<div class="sp-uc-icon">🛍️</div>
<h3>Price Comparison</h3>
<p>Search and compare product prices across platforms to build a price comparison tool.</p>
</div>
</div>
</div>
</section>
<section class="sp-section sp-bg-white">
<div class="sp-container">
<div class="sp-header">
<h2>Core Parameters</h2>
<p>Flexibly customize search requests and precisely control output</p>
</div>
<div class="sp-param-grid">
<div class="sp-param-card">
<div class="sp-param-val">q</div>
<h3>Search Keywords</h3>
<p class="param-desc">The keywords or query statements to search for, supporting Google search syntax.</p>
</div>
<div class="sp-param-card">
<div class="sp-param-val">number</div>
<h3>Number of Results</h3>
<p class="param-desc">The number of search results to return, affecting billing tiers (≤10 or >10).</p>
</div>
<div class="sp-param-card">
<div class="sp-param-val">gl</div>
<h3>Country/Region</h3>
<p class="param-desc">Specify the target country for the search (e.g., <code>us</code>, <code>cn</code>, <code>jp</code>) to get localized results.</p>
</div>
<div class="sp-param-card">
<div class="sp-param-val">hl</div>
<h3>Language</h3>
<p class="param-desc">Specify the language of the search results (e.g., <code>en</code>, <code>zh-CN</code>, <code>ja</code>).</p>
</div>
<div class="sp-param-card">
<div class="sp-param-val">type</div>
<h3>Search Type</h3>
<p class="param-desc">Search types: web (search), images (images), news (news), etc.</p>
</div>
<div class="sp-param-card">
<div class="sp-param-val">start</div>
<h3>Starting Position</h3>
<p class="param-desc">The offset of search results, used for pagination to get more results.</p>
</div>
</div>
</div>
</section>
<section class="sp-section sp-bg-gray">
<div class="sp-container">
<div class="sp-header">
<h2>SERP API Pricing</h2>
<p>Charged by the number of requests, simple and transparent.</p>
</div>
<div class="sp-price-table-wrap">
<table class="sp-price-table">
<thead>
<tr>
<th>Request Type</th>
<th>Number of Results</th>
<th>Price per Request</th>
</tr>
</thead>
<tbody>
<tr>
<td>Google Search</td>
<td>≤ 10 results</td>
<td class="td-price">$0.00095</td>
</tr>
<tr>
<td>Google Search</td>
<td>> 10 results</td>
<td class="td-price">$0.0019</td>
</tr>
</tbody>
</table>
</div>
<p class="sp-price-note">💡 Charged per request, no monthly fees, no hidden charges. Bulk purchases can enjoy additional discounts.</p>
</div>
</section>
<section class="sp-section sp-bg-white">
<div class="sp-container-narrow">
<div class="sp-header">
<h2>Frequently Asked Questions</h2>
<p>Common questions about using the SERP API</p>
</div>
<div class="sp-faq-list">
<div class="sp-faq-item">
<div class="sp-faq-q"><span>Is the data returned by the SERP API real-time?</span><span class="sp-faq-chev">›</span></div>
<div class="sp-faq-a"><p>Yes, each request queries the Google search engine in real-time and returns the latest results, not cached data.</p></div>
</div>
<div class="sp-faq-item">
<div class="sp-faq-q"><span>What search types are supported?</span><span class="sp-faq-chev">›</span></div>
<div class="sp-faq-a"><p>Supports various types such as web search (search), image search (images), news search (news), etc., switched via the <code>type</code> parameter.</p></div>
</div>
<div class="sp-faq-item">
<div class="sp-faq-q"><span>How to get more search results?</span><span class="sp-faq-chev">›</span></div>
<div class="sp-faq-a"><p>Use the <code>number</code> parameter to control the number of results returned each time, combined with the <code>start</code> parameter for pagination to obtain a large number of search results.</p></div>
</div>
<div class="sp-faq-item">
<div class="sp-faq-q"><span>Can I search for results from specific countries/languages?</span><span class="sp-faq-chev">›</span></div>
<div class="sp-faq-a"><p>Yes. Specify the country for the search using the <code>gl</code> parameter (e.g., <code>us</code>), and the result language using the <code>hl</code> parameter (e.g., <code>en</code>) to accurately locate the results you need.</p></div>
</div>
<div class="sp-faq-item">
<div class="sp-faq-q"><span>Is it suitable for use with AI Agents?</span><span class="sp-faq-chev">›</span></div>
<div class="sp-faq-a"><p>Very suitable. The SERP API returns structured JSON data, which can be directly used as a tool for LLM Agents. Ace Data Cloud also provides an MCP Server wrapper that can be directly called in AI like Claude, ChatGPT, etc.</p></div>
</div>
</div>
</div>
</section>
<section class="sp-section sp-bg-gray">
<div class="sp-container">
<div class="sp-header">
<h2>Explore More AI Services</h2>
<p>Ace Data Cloud offers various AI service APIs</p>
</div>
<div class="sp-rel-grid">
<a class="sp-rel-card" href="/services/claude">
<span class="sp-rel-icon">🟠</span>
<div class="sp-rel-info"><h3>Claude</h3><p>Anthropic AI</p></div>
<span class="sp-rel-arrow">→</span>
</a>
<a class="sp-rel-card" href="/services/gemini">
<span class="sp-rel-icon">💎</span>
<div class="sp-rel-info"><h3>Gemini</h3><p>Google AI</p></div>
<span class="sp-rel-arrow">→</span>
</a>
<a class="sp-rel-card" href="/services/midjourney">
<span class="sp-rel-icon">🎨</span>
<div class="sp-rel-info"><h3>Midjourney</h3><p>AI Painting</p></div>
<span class="sp-rel-arrow">→</span>
</a>
<a class="sp-rel-card" href="/services/suno">
<span class="sp-rel-icon">🎵</span>
<div class="sp-rel-info"><h3>Suno</h3><p>AI Music</p></div>
<span class="sp-rel-arrow">→</span>
</a>
</div>
</div>
</section>
<section class="serp-cta">
<div class="sp-container">
<h2>Start Using SERP API Now</h2>
<p>Efficiently obtain Google search results to empower your applications.</p>
<div class="sp-actions">
<a class="btn-cta-light" href="/apis/serp-google">Get Started →</a>
<a class="btn-cta-ghost" href="/support">Contact Support</a>
</div>
</div>
</section>
</div>

## Quick Start

- Base URL: [https://api.acedata.cloud](https://api.acedata.cloud)
- Service page: [Search Engine on Ace Data Cloud](https://platform.acedata.cloud/service/serp)
- Docs: [Developer documentation](https://docs.acedata.cloud)

```bash
curl --request POST "https://api.acedata.cloud/serp/google" \
  --header "Authorization: Bearer YOUR_API_KEY" \
  --header "Content-Type: application/json" \
  --data '{}'
```

## APIs and Guides

Explore the supported endpoints and integration guides for Search Engine.

| API | Path | Integration Guidance |
| ---- | ---- | ------------ |
| [Google SERP API](https://platform.acedata.cloud/documents/44c86226-8eaa-49bf-85f3-1fae8d2e23f1) | `/serp/google` | [Google SERP API Integration Guide](https://platform.acedata.cloud/documents/cc2ce913-df8f-4d22-a051-93fa33b2e51b) |

## Related Resources

- [Ace Data Cloud Developer Platform](https://platform.acedata.cloud)
- [Ace Data Cloud Docs](https://docs.acedata.cloud)
- [Status Page](https://status.acedata.cloud)
- [Ace Data Cloud GitHub Organization](https://github.com/AceDataCloud)

## Support

If you meet any issue, please check [support info](https://platform.acedata.cloud/support) or browse the latest documentation on [docs.acedata.cloud](https://docs.acedata.cloud).
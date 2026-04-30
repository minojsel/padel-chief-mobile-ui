# Padel Chief — Design System Reference

**Covers:** `index.html` (Auth) · `padel-chief-dashboard.html` · `padel-chief-browse.html` · `padel-chief-rankings.html`

---

## 1. Typography

### 1.1 Font

| Property | Value |
|----------|-------|
| Family | `'Plus Jakarta Sans', sans-serif` (Google Fonts) |
| Weights loaded | 400 · 500 · 600 · 700 · 800 |
| Icon set | Material Symbols Outlined (variable font, `wght,FILL@100..700,0..1`) |

Default icon settings applied globally:
```css
.material-symbols-outlined {
  font-variation-settings: 'FILL' 0, 'wght' 300, 'GRAD' 0, 'opsz' 24;
}
```

---

### 1.2 Type Scale

This is the **complete, normalized type system** used across all pages. Every text element maps to exactly one of these levels.

| Level | Name | Size | Weight | Letter-spacing | Line-height | Casing |
|-------|------|------|--------|----------------|-------------|--------|
| `display` | Display | 28px | 700 | −0.02em | 1.15 | Sentence |
| `h1` | Heading 1 | 24px | 800 | −0.02em | 1.0 | Sentence |
| `h2` | Heading 2 | 17px | 700 | −0.01em | 1.2 | Sentence |
| `h3` | Heading 3 | 15px | 700 | −0.01em | 1.25 | Sentence |
| `title` | Title | 13px | 700 | 0 | 1.3 | Sentence |
| `body-lg` | Body Large | 14px | 500 | 0 | 1.5 | Sentence |
| `body` | Body | 13px | 500 | 0 | 1.5 | Sentence |
| `body-sm` | Body Small | 12px | 500 | 0 | 1.5 | Sentence |
| `label` | Label | 12px | 600 | 0 | 1.0 | Sentence |
| `label-sm` | Label Small | 11px | 600 | 0 | 1.0 | Sentence |
| `overline` | Overline | 10px | 700 | 0.10em | 1.0 | ALL CAPS |
| `caption` | Caption | 9px | 600 | 0.06em | 1.0 | Sentence or ALL CAPS |
| `nano` | Nano | 8px | 700 | 0.05em | 1.0 | ALL CAPS |

> **Color note:** Size and weight are defined in the type scale. Text color is always set by the component using it — see Section 3.

---

### 1.3 Type Scale Usage Map

Every text element in the app, mapped to its type level.

#### Display (28px / 700 / −0.02em)
| Element | Page | CSS class |
|---------|------|-----------|
| Auth screen heading ("Sign in", "Create account") | index | `.auth-heading` |

#### Heading 1 (24px / 800 / −0.02em)
| Element | Page | CSS class |
|---------|------|-----------|
| Browse page title ("Browse") | browse | `.browse-title` |
| Rankings page title ("Rankings") | rankings | `.header-title` |

#### Heading 2 (17px / 700 / −0.01em)
| Element | Page | CSS class |
|---------|------|-----------|
| User's display name in top bar ("Marco Silva") | dashboard | `.top-bar-name` |
| Dashboard section headings ("Your stats", "Upcoming Tournaments") | dashboard | `.section-title` |
| Notification page title ("Notifications") | dashboard | `.notif-page-title` |
| Bottom sheet title ("Filters", "Sort & Filter") | browse / rankings | `.sheet-title` |
| Match score — large number | dashboard | `.match-score-big` (22px — *see note*) |

> ⚠️ `.match-score-big` is 22px/800, used only for live match numerals. It's a display number, not a heading. Treat it as a data display variant, not a typography level.

#### Heading 3 (15px / 700 / −0.01em)
| Element | Page | CSS class |
|---------|------|-----------|
| Tournament / card names | dashboard | `.tournament-name` |
| Browse card names | browse | `.t-card-name` |
| Quick-action banner title | dashboard | `.quick-banner-title` |
| Primary button label | index | `.btn-primary` |

#### Title (13px / 700)
| Element | Page | CSS class |
|---------|------|-----------|
| Ongoing match — tournament name | dashboard | `.ongoing-tournament-name` |
| Activity item title | dashboard | `.activity-title` |
| Rankings row — player name | rankings | `.rank-row-name` |
| Podium section — the "Ranked" divider title context | rankings | — |
| Mini card title (tournament) | browse | `.mini-card-title` |
| Notifications — item title | dashboard | `.notif-item-title` |

#### Body Large (14px / 500)
| Element | Page | CSS class |
|---------|------|-----------|
| Form inputs (email, password, name) | index | `.form-input` |
| Search input | browse | `.search-input` |
| Outline button label | index | `.btn-outline` |
| Sheet apply button label | all | `.sheet-apply` (14px/700 — weight upgraded for button) |

#### Body (13px / 500)
| Element | Page | CSS class |
|---------|------|-----------|
| Auth subheading | index | `.auth-subheading` |
| General descriptions, center copy | index | `.center-copy` |
| Auth footer span ("Don't have an account?") | index | `.auth-footer span` |
| Checkbox label text | index | `.checkbox-text` |

#### Body Small (12px / 500)
| Element | Page | CSS class |
|---------|------|-----------|
| Tournament meta items (date, location, players) | dashboard / browse | `.tournament-meta-item`, `.t-meta-item` |
| Match team names | dashboard | `.match-team-name` |
| Ongoing location | dashboard | `.ongoing-location` |
| Activity subtitle | dashboard | `.activity-subtitle` |
| Mini card subtitle | browse | `.mini-card-sub` |

#### Label (12px / 600)
| Element | Page | CSS class |
|---------|------|-----------|
| Filter chips (default state) | browse / rankings | `.filter-chip`, `.chip` |
| Sport / segmented toggle buttons | browse / rankings | `.sport-btn`, `.seg-btn` |
| Sheet chips (options) | all | `.sheet-chip` |
| Sort chips | browse | `.sort-chip` |
| Section "See all" link | dashboard | `.section-link` |
| Tournament CTA ("View →") | dashboard / browse | `.tournament-cta`, `.t-cta` |
| Cancel search button | browse | `.search-cancel-btn` |
| Sheet reset link | all | `.sheet-reset-link` |
| Auth link ("Forgot password?") | index | `.auth-link` |

#### Label Small (11px / 600)
| Element | Page | CSS class |
|---------|------|-----------|
| Browse count ("14 tournaments") | browse | `.browse-count` |
| Rankings subtitle ("8 players · Sri Lanka") | rankings | `.header-subtitle` |
| Top bar greeting line ("Good evening") | dashboard | `.top-bar-hello` |
| Player count in card footer | dashboard / browse | `.tournament-players-count`, `.t-player-count` |
| Banner subtitle ("Find opponents near you") | dashboard | `.quick-banner-sub` |
| Activity subtitle | dashboard | `.activity-subtitle` |
| Notifications subtitle | dashboard | `.notif-item-sub` |
| Win streak badge text | dashboard | `.win-streak-badge` |
| Set chip score | dashboard | `.set-score-chip .set-val` |

#### Overline (10px / 700 / 0.10em / ALL CAPS)
| Element | Page | CSS class |
|---------|------|-----------|
| Form field labels ("EMAIL ADDRESS") | index | `.form-label` |
| Stat card labels ("WIN RATE", "MATCHES") | dashboard | `.stat-label` |
| Ongoing set info ("SERVING · SET 2") | dashboard | `.ongoing-set-info` |
| Match badge text ("LIVE", "SCHEDULED") | dashboard | `.match-badge` |
| Tournament format badge | dashboard | `.tournament-format-badge` |
| Status badge | browse | `.status-badge` |
| Sport badge ("PADEL", "PICKLEBALL") | browse / rankings / dashboard | `.sport-badge`, `.sport-pill` |
| Sheet section titles ("LOCATION", "FORMAT") | all | `.sheet-section-title` |
| Set chip label ("S1", "S2") | dashboard | `.set-score-chip .set-label` |
| Podium confidence label | rankings | `.podium-conf` *(8px — nano)* |
| Result filter tag | browse | `.result-filter-tag` |

#### Caption (9px / 600 / 0.06em)
| Element | Page | CSS class |
|---------|------|-----------|
| Bottom nav labels ("Home", "Browse") | all | `.nav-item-label` |
| Your Position label ("YOUR POSITION") | rankings | `.your-pos-label` |
| Rankings section divider ("Ranked") | rankings | `.rank-list-divider span` |
| Stat key in expanded rows | rankings | `.stat-key`, `.podium-stat-key` |

#### Nano (8px / 700 / 0.05em / ALL CAPS)
| Element | Page | CSS class |
|---------|------|-----------|
| Confidence labels ("HIGH", "MEDIUM", "LOW") | rankings | `.podium-conf`, `.rank-row-conf` |
| Filter badge count | browse / rankings | `.filter-badge` |

---

### 1.4 Icon Font Variation Settings

| Context | `font-variation-settings` |
|---------|--------------------------|
| Default (all icons) | `'FILL' 0, 'wght' 300, 'GRAD' 0, 'opsz' 24` |
| Active nav icon | `'FILL' 1, 'wght' 200` |
| Filled decorative icon (badges, labels, stat icons) | `'FILL' 1, 'wght' 400` |
| Win streak badge fire icon | `'FILL' 1, 'wght' 600` |
| Checkbox checkmark | `'FILL' 1, 'wght' 700` |
| Expand/collapse chevron | `'FILL' 0, 'wght' 300` |

---

## 2. Colour Tokens

### 2.1 CSS Custom Properties (`:root`)

All four files share the same token set.

| Token | Hex | rgba |
|-------|-----|------|
| `--surface` | `#FFFFFF` | `rgba(255, 255, 255, 1.0)` |
| `--background` | `#E8EEF5` ¹ | `rgba(232, 238, 245, 1.0)` |
| `--on-background` | `#0F172A` | `rgba(15, 23, 42, 1.0)` |
| `--on-surface` | `#0F172A` | `rgba(15, 23, 42, 1.0)` |
| `--on-surface-variant` | `#475569` | `rgba(71, 85, 105, 1.0)` |
| `--primary` | `#125fa9` | `rgba(18, 95, 169, 1.0)` |
| `--primary-container` | `#2268b2` | `rgba(34, 104, 178, 1.0)` |
| `--on-primary-container` | `#FFFFFF` | `rgba(255, 255, 255, 1.0)` |
| `--secondary-fixed` | `#d8ef00` | `rgba(216, 239, 0, 1.0)` |
| `--on-secondary-fixed` | `#1a1e00` | `rgba(26, 30, 0, 1.0)` |
| `--outline` | `#94A3B8` | `rgba(148, 163, 184, 1.0)` |
| `--outline-variant` | `#E2E8F0` | `rgba(226, 232, 240, 1.0)` |
| `--surface-container-lowest` | `#FFFFFF` | `rgba(255, 255, 255, 1.0)` |
| `--surface-container-low` | `#F8FAFC` | `rgba(248, 250, 252, 1.0)` |
| `--surface-container` | `#F1F5F9` | `rgba(241, 245, 249, 1.0)` |
| `--surface-container-high` | `#E2E8F0` | `rgba(226, 232, 240, 1.0)` |
| `--surface-container-highest` | `#F1F5F9` | `rgba(241, 245, 249, 1.0)` |
| `--error` | `#B91C1C` | `rgba(185, 28, 28, 1.0)` |
| `--error-container` | `#FEE2E2` | `rgba(254, 226, 226, 1.0)` |
| `--on-error-container` | `#991B1B` | `rgba(153, 27, 27, 1.0)` |
| `--inverse-surface` | `#0F172A` | `rgba(15, 23, 42, 1.0)` |
| `--inverse-on-surface` | `#F8FAFC` | `rgba(248, 250, 252, 1.0)` |
| `--pickle` ² | `#0d9488` | `rgba(13, 148, 136, 1.0)` |
| `--pickle-bg` ² | — | `rgba(13, 148, 136, 0.08)` |
| `--live` ² | `#dc2626` | `rgba(220, 38, 38, 1.0)` |
| `--live-bg` ² | — | `rgba(239, 68, 68, 0.08)` |
| `--completed` ² | `#475569` | `rgba(71, 85, 105, 1.0)` |
| `--completed-bg` ² | — | `rgba(71, 85, 105, 0.08)` |

> ¹ `index.html` uses `--background: #F8FAFC` — lighter, for the auth screen context.  
> ² Browse and Rankings only.

### 2.2 Semantic / Hard-coded Colours

| Purpose | Hex | rgba |
|---------|-----|------|
| Canvas (studio background) | `#0a0c10` | `rgba(10, 12, 16, 1.0)` |
| Phone notch | `#0F172A` | `rgba(15, 23, 42, 1.0)` |
| Lime (brand accent — secondary fixed) | `#d8ef00` | `rgba(216, 239, 0, 1.0)` |
| Lime dark (text on light bg) | `#6b7f00` | `rgba(107, 127, 0, 1.0)` |
| Lime mid (icon on lime bg) | `#89a300` | `rgba(137, 163, 0, 1.0)` |
| Positive / Win / High confidence | `#0d9488` | `rgba(13, 148, 136, 1.0)` |
| Negative / Loss / Low confidence | `#dc2626` | `rgba(220, 38, 38, 1.0)` |
| Warning / Medium confidence | `#d97706` | `rgba(217, 119, 6, 1.0)` |
| Gold podium — gradient start | `#fbbf24` | `rgba(251, 191, 36, 1.0)` |
| Gold podium — gradient end | `#d97706` | `rgba(217, 119, 6, 1.0)` |
| Silver podium — gradient start | `#e2e8f0` | `rgba(226, 232, 240, 1.0)` |
| Silver podium — gradient end | `#94a3b8` | `rgba(148, 163, 184, 1.0)` |
| Bronze podium — gradient start | `#d4a27a` | `rgba(212, 162, 122, 1.0)` |
| Bronze podium — gradient end | `#b07850` | `rgba(176, 120, 80, 1.0)` |

---

## 3. Component Colour Reference

### 3.1 Backgrounds & Borders

| Component | Background | Border |
|-----------|------------|--------|
| Page background | `#E8EEF5` | — |
| Surface (cards, sheets) | `#FFFFFF` | — |
| Sticky header (frosted) | `rgba(248, 250, 252, 0.92)` + `blur(20px)` | — |
| Bottom nav (frosted) | `rgba(255, 255, 255, 0.95)` + `blur(24px)` | — |
| Sheet overlay | `rgba(15, 23, 42, 0.36)` + `blur(2px)` | — |
| Icon button (default) | `#F1F5F9` | — |
| Icon button (active) | `rgba(18, 95, 169, 0.10)` | — |
| Segmented toggle container | `#F1F5F9` | — |
| Segmented button — active pill | `#FFFFFF` | — |
| Filter chip — default | `#FFFFFF` | — |
| Filter chip — active (padel/default) | `#2268b2` | — |
| Filter chip — active (live) | `#dc2626` | — |
| Filter chip — active (completed) | `#475569` | — |
| Sheet chip — default | `#F1F5F9` | — |
| Sheet chip — selected | `#2268b2` | — |
| Stat card | `#FFFFFF` | — |
| Tournament card | `#FFFFFF` | — |
| Quick-action banner | `linear-gradient(135deg, #0d1f38, #163d6a)` | — |
| Your-Position card (rankings) | `rgba(18, 95, 169, 0.05)` | `1.5px solid rgba(18,95,169,0.16)` |
| Me-row highlight (rankings list) | `rgba(18, 95, 169, 0.04)` | — |
| Rank list wrapper | `#FFFFFF` | — |
| Podium card — Gold (#1) | `rgba(217, 119, 6, 0.07)` | `1.5px solid rgba(217,119,6,0.22)` |
| Podium card — Silver (#2) | `rgba(100, 116, 139, 0.06)` | `1.5px solid rgba(100,116,139,0.18)` |
| Podium card — Bronze (#3) | `rgba(176, 120, 80, 0.06)` | `1.5px solid rgba(176,120,80,0.18)` |
| Rank badge — Gold | `linear-gradient(135deg, #fbbf24, #d97706)` | — |
| Rank badge — Silver | `linear-gradient(135deg, #e2e8f0, #94a3b8)` | — |
| Rank badge — Bronze | `linear-gradient(135deg, #d4a27a, #b07850)` | — |
| Form input (default) | `#F1F5F9` | none |
| Form input (focused) | `#FFFFFF` | `2px solid #125fa9` |
| Primary button | `linear-gradient(135deg, #2268b2, #125fa9)` | — |
| Outline / social button | `#F1F5F9` | — |
| Checkbox — unchecked | `#FFFFFF` | `2px solid #E2E8F0` |
| Checkbox — checked | `#2268b2` | `2px solid #2268b2` |
| Win streak badge | `rgba(216, 239, 0, 0.15)` | — |
| Sport badge — padel | `rgba(18, 95, 169, 0.08)` | — |
| Sport badge — pickleball | `rgba(13, 148, 136, 0.08)` | — |
| Tournament format badge | `rgba(18, 95, 169, 0.06)` | — |
| Tournament CTA button | `rgba(18, 95, 169, 0.07)` | — |
| Activity icon — win | `rgba(13, 148, 136, 0.10)` | — |
| Activity icon — loss | `rgba(239, 68, 68, 0.08)` | — |
| Activity icon — event | `rgba(18, 95, 169, 0.08)` | — |
| Activity result — win | `rgba(13, 148, 136, 0.08)` | — |
| Activity result — loss | `rgba(239, 68, 68, 0.06)` | — |
| Stat icon — blue | `rgba(18, 95, 169, 0.10)` | — |
| Stat icon — lime | `rgba(216, 239, 0, 0.18)` | — |
| Stat icon — teal | `rgba(13, 148, 136, 0.10)` | — |
| Live badge | `rgba(239, 68, 68, 0.08)` | — |

### 3.2 Text Colors by Component

| Component | Color token | Hex |
|-----------|-------------|-----|
| Primary text (headings, names, data) | `--on-surface` / `--on-background` | `#0F172A` |
| Secondary text (subtitles, meta, captions) | `--on-surface-variant` | `#475569` |
| Link / interactive accent | `--primary` | `#125fa9` |
| Placeholder text | `--outline` | `#94A3B8` |
| Text on filled buttons | `--on-primary-container` | `#FFFFFF` |
| Text on banner | — | `#FFFFFF` |
| Banner subtitle | — | `rgba(255, 255, 255, 0.50)` |
| Rating numbers | `--primary` | `#125fa9` |
| Positive / Win / High conf. | — | `#0d9488` |
| Negative / Loss / Low conf. | — | `#dc2626` |
| Warning / Medium conf. | — | `#d97706` |
| Silver rank badge number | — | `#475569` |
| Rank position number (list) | `--on-surface-variant` | `#475569` |
| Live status text | `--live` | `#dc2626` |
| Pickleball accent text | `--pickle` | `#0d9488` |
| Lime accent (streak badge) | — | `#6b7f00` |
| Nav — active | `--primary` | `#125fa9` |
| Nav — inactive | `--on-surface-variant` | `#475569` |
| Notification badge | `--error` | `#B91C1C` |
| Search highlight mark text | `--primary` | `#125fa9` |
| Search highlight mark bg | — | `rgba(18, 95, 169, 0.10)` |

### 3.3 Shadows & Elevation

| Component | Box Shadow |
|-----------|------------|
| Stat card | `0 1px 4px rgba(15,23,42,0.07), 0 1px 2px rgba(15,23,42,0.04)` |
| Tournament / browse card | `0 1px 4px rgba(15,23,42,0.07), 0 1px 2px rgba(15,23,42,0.04)` |
| Rank list wrapper | `0 1px 3px rgba(15,23,42,0.06)` |
| Bottom sheet | `0 -16px 48px rgba(0,0,0,0.12)` |
| Bottom nav | `0 -8px 32px rgba(0,0,0,0.04)` |
| Primary button | `0 8px 24px rgba(18,95,169,0.25)` |
| Segmented active pill | `0 2px 8px rgba(0,0,0,0.07)` |
| Rank badge — gold | `0 2px 8px rgba(217,119,6,0.40)` |
| Rank badge — silver | `0 2px 6px rgba(100,116,139,0.30)` |
| Rank badge — bronze | `0 2px 6px rgba(176,120,80,0.30)` |
| Podium avatar | `0 2px 8px rgba(0,0,0,0.10)` |
| Phone frame (mockup only) | `0 40px 80px rgba(0,0,0,0.50)` |

### 3.4 Dividers

| Context | Color | Hex | rgba |
|---------|-------|-----|------|
| Default row separator / card divider | `--outline-variant` | `#E2E8F0` | `rgba(226, 232, 240, 1.0)` |
| Sheet handle pill | `--outline-variant` | `#E2E8F0` | `rgba(226, 232, 240, 1.0)` |
| Avatar ring (stacked player avatars) | `--surface` | `#FFFFFF` | `rgba(255, 255, 255, 1.0)` |
| Podium stat grid inner border | — | — | `rgba(0, 0, 0, 0.07)` |

---

## 4. Bottom Navigation

| State | Icon | Label |
|-------|------|-------|
| Active | 24px · `#125fa9` · `FILL 1, wght 200` | 9px / 600 · `#125fa9` |
| Inactive | 24px · `#475569` · `FILL 0, wght 300` | 9px / 600 · `#475569` |
| Create (centre) | 28px · `#475569` | — |

Background: `rgba(255,255,255,0.95)` + `backdrop-filter: blur(24px)`  
Border-radius (top-left / top-right): `28px`

---

## 5. Gradients

| Name | Value |
|------|-------|
| Primary button | `linear-gradient(135deg, #2268b2, #125fa9)` |
| Quick-action banner | `linear-gradient(135deg, #0d1f38, #163d6a)` |
| Splash screen | `linear-gradient(170deg, #081525 0%, #0d1f38 35%, #112d50 65%, #163d6a 100%)` |
| Gold rank badge | `linear-gradient(135deg, #fbbf24, #d97706)` |
| Silver rank badge | `linear-gradient(135deg, #e2e8f0, #94a3b8)` |
| Bronze rank badge | `linear-gradient(135deg, #d4a27a, #b07850)` |
| Banner glow orb | `radial-gradient(circle, rgba(216,239,0,0.08) 0%, transparent 70%)` |

---

## 6. Sticky Header (all main pages)

All three main pages use an identical frosted glass header spec:

```css
background: rgba(248, 250, 252, 0.92);
backdrop-filter: blur(20px);
-webkit-backdrop-filter: blur(20px);
position: sticky;
top: 0;
z-index: 50;
```

Top padding before content: `44px` (accounts for status bar).

---

## 7. Border Radii (quick reference)

| Component | Radius |
|-----------|--------|
| Phone frame (mockup) | 44px |
| Bottom sheet | 28px 28px 0 0 |
| Bottom nav | 28px 28px 0 0 |
| Stat cards (dashboard) | 20px |
| Tournament cards (browse) | 20px |
| Browse/rankings cards | 18–20px |
| Rank list wrapper | 16px |
| Podium cards | 18px |
| Quick-action banner | 20px |
| Icon button | 12px |
| Segmented toggle container | 14px |
| Segmented active pill | 10px |
| Filter / sheet chips | 9999px (pill) |
| Form inputs | 14px |
| Primary button | 16px |
| Social / outline button | 14px |
| Activity icon | 12px |
| Rank badge (podium) | 50% (circle) |
| Podium avatar | 50% (circle) |
| Notification badge | 50% (circle) |

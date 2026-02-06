# Tokamak HR - Monthly Activity Report System

Tokamak Network 팀원별 월간 활동 리포트 생성 도구

## Features

- Google Drive, GitHub, Slack, Notion 활동 통합 분석
- 팀원별 활동 점수 산출 및 랭킹
- Markdown 리포트 + HTML 대시보드 생성

## Usage

```bash
python3 generate_monthly_report.py <csv_file>
```

### Example

```bash
python3 generate_monthly_report.py custom_export_2026-01-01_2026-01-31.csv
```

### Output

- `monthly_report_<period>.md` - Markdown 리포트
- `monthly_report_<period>.html` - 웹 대시보드

## Data Source

통합 CSV 파일 (source 컬럼으로 구분):
- `drive` - Google Drive 편집 활동
- `github` - Commits, PRs, Reviews
- `slack` - Messages
- `notion` - Pages, Content edits

## Scoring System

| Activity | Points |
|----------|--------|
| Drive Edit | 2 |
| GitHub Commit | 3 |
| GitHub PR | 5 |
| GitHub Review | 4 |
| Slack Message | 1 |
| Notion Page | 3 |
| Notion Edit | 2 |

## Files

```
tokamak-hr/
├── generate_monthly_report.py    # Main script
├── monthly_report_*.md           # Generated MD reports
├── monthly_report_*.html         # Generated HTML dashboards
└── README.md
```

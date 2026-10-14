# claude-plugins

duddudcns의 개인용 Claude Code 및 Codex 플러그인 마켓플레이스입니다. 코드는 각 플러그인 레포에 있고 이 저장소에는 카탈로그만 둡니다.

## Claude Code

Claude Code는 `.claude-plugin` 카탈로그를 사용합니다.

```bash
claude plugin marketplace add duddudcns/claude-plugins
claude plugin install usage-band@duddudcns
```

## Codex

Codex는 `.agents` 카탈로그를 사용합니다.

```bash
codex plugin marketplace add duddudcns/claude-plugins --ref main
codex plugin add NAME@duddudcns
```

`NAME`을 설치할 플러그인 이름으로 바꾸세요.

## Claude와 Codex 호환성

| 플러그인 | Codex 호환성 및 제한 |
| --- | --- |
| `llm-wiki` | Codex 네이티브 스킬과 MCP를 제공합니다. 위키 데이터는 프로젝트의 `ai-wiki/` 또는 `raw/`, `wiki/`, `.llmw/`에 저장되며 플러그인 캐시 안에는 저장되지 않습니다. |
| `anti-slop` | 재사용 가능한 스킬과 Node 스캐너를 제공합니다. Claude 슬래시 명령, 에이전트, 자동 훅의 Codex 지원은 확인되지 않았습니다. |
| `vbq` | 재사용 가능한 스킬과 CLI를 제공합니다. Node와 `DNAKode.VbNet.Lsp` 0.1.10 이상이 필요합니다. Windows에서는 전체 shim 경로 `bin/vbq.cmd`를 사용합니다. |
| `fast-jev-compaction` | 설치는 가능하지만 Claude의 `PreCompact` 기반 압축 훅은 Codex에서 동작하지 않습니다. |
| `subagents` | 패키지 설치는 가능하지만 Claude 역할 메타데이터와 게이트는 Codex에 직접 이식되지 않습니다. Codex `subagents-luna`는 별도 유지가 필요합니다. |
| `usage-band` | Claude 전용 사용량 UI 훅입니다. Codex 카탈로그에는 등록하지 않았습니다. |

설치한 뒤 새 채팅을 시작하거나 앱을 다시 시작하세요.


# Decision Logging SOP

## Purpose
Track every decision with minimal tokens for audit trail and accountability.

## System Rules

### 1. Git Commit After Every Response
- **Trigger**: Every AI response completion
- **Action**: Commit conversation logs to life-os-logs repository
- **Format**: "Log: [brief description] - [timestamp]"

### 2. Decision Log Entry
- **Trigger**: Any decision made during conversation
- **Format**: `[TIMESTAMP] | [DECISION] | [REASONING] | [AUTHORITY]`
- **Location**: `/PrinciplesOS/decision-log.md`

### 3. Lightweight Logging System
- **Active Log**: Current decisions in main decision-log.md
- **Archive Threshold**: 50 entries triggers archival
- **Archive Format**: `/PrinciplesOS/archived-decisions-YYYY-MM.md`

### 4. Minimal Token Reasoning
- **Goal**: Maximum 15 tokens per reasoning entry
- **Format**: Action-oriented, concise justification
- **Example**: "Reduce cognitive load for ADHD"

## Authorities Cited
- **Mathieu Directives**: Presidential productivity requirements
- **Smart Friend Analysis**: ADHD productivity systems
- **Team Topologies**: Cognitive load principles

## Accountability
- Every response logged
- Every decision tracked
- Weekly review of log completeness
- Monthly archive maintenance

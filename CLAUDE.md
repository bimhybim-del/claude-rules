# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

This repository stores generic Claude AI rules intended to be shared across all repositories. The primary artifact is `RULES.md`, which contains common rules for Claude instances operating in other codebases.

## Repository Structure

- `RULES.md` — the canonical rules document; add new shared Claude rules here
- `.github/workflows/semgrep.yml` — Semgrep security scan triggered on PRs to `main`, `master`, or `develop`, and on a weekly schedule (Sundays 03:30 UTC); calls the reusable workflow at `jupitermoney/security-automations/.github/workflows/semgrep-reusable-workflow.yml@develop`

## CI

There is no build system or test suite. The only automated workflow is the Semgrep scan. Required secrets for the workflow: `SEMGREP_API_URL`, `SEMGREP_SLACK_BOT_TOKEN`, `SEMGREP_SLACK_SIGNING_SECRET`, `SEMGREP_GITHUB_TOKEN`, `SEMGREP_API_KEY`.

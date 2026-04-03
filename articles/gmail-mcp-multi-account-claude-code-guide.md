# Gmail MCP for Claude Code: Multi-Account Setup + 5 Workflows

**URL:** https://buildtolaunch.substack.com/p/gmail-mcp-multi-account-claude-code-guide  
**Published:** March 28, 2026  
**Word count:** ~3,278  
**Engagement:** 23 likes, 4 restacks  
**Access:** Paid

---

## Summary

Connecting one Gmail account to Claude Code is straightforward. Connecting multiple accounts reliably — without constant re-authentication, account mixups, or broken routing — is where most setups quietly break. This article documents Jenny's multi-account Gmail MCP setup for Claude Code, the exact install flow, and 5 real workflows she runs across 4 Gmail accounts (personal, newsletter, business, payments).

The motivating scenario: tax season with income from 6+ platforms landing in 4 different inboxes. Before the setup, reconciling receipts meant logging into each account separately, searching, and cross-referencing dates. After: Claude moves through all four accounts in sequence, fetches what's needed, and stores it locally — 918 unread messages processed down to 7 action items in 40 seconds.

---

## Multi-Account Architecture

The problem with naive multi-account setups: each connection uses separate OAuth credentials, which breaks when Claude needs to switch accounts within a single session. Jenny's solution: one Google Cloud project, named connection identifiers per account, and a configuration pattern that makes account routing explicit and durable across sessions.

---

## 5 Workflows Worth Running First

1. **Receipt extractor** — scans all inboxes for receipts matching date range and vendor patterns; extracted $986.41 in one run for tax documentation
2. **Collab pitch triage** — filters collab/partnership emails by criteria, returns decision-ready summaries rather than forwarding everything
3. **Inbox zero sequence** — classify → archive → draft responses in one Claude Code session across all accounts
4. **Subscriber surge detector** — monitors for unusual Substack subscriber notification spikes; caught 28 new subscribers before manual review would have noticed
5. **Morning brief** — all 4 accounts, returns only items requiring attention; 7 items from 918+ unread in 40 seconds

---

## Setup Guide

Step-by-step walkthrough for: Google Cloud OAuth configuration, named connection setup per account, Claude Code MCP config structure, and the specific changes that make multi-account routing reliable (vs. the naive single-account setup that breaks silently when more accounts are added).

---

## Key Sections

1. What You Can Actually Automate with Gmail MCP
2. When Gmail MCP Needs Multiple Gmail Accounts
3. 5 Gmail MCP Workflows Worth Running First
4. Gmail MCP Multi-Account Setup for Claude Code
5. Config template + 5-prompt pack + 12 more automation ideas

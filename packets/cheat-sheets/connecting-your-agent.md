# Cheat Sheet: Connecting Your Agent

Every company system is an MCP server at one URL. This page gets any agent connected in about three minutes per system.

## The URL pattern

```
https://parade.paulcheek.com/mcp/<system>/<session-slug>
```

Your URLs come from `/start`: choose a department, or take The Whole Council, and one click mints your private session and lists every connector URL. The session slug is the credential, so treat it like one. The systems and their path segments:

| System | Path segment |
| - | - |
| AirBook CRM | crm |
| AirWare ERP 4.7 | erp |
| FloatDesk | support |
| AirMail | comms |
| The Breeze | social |
| Balloon Payments | finance |
| The Gary Graph | gary |

The `/start` page and the Field Guide (`/guide`) both list which systems are yours. Every department has AirMail and the Gary Graph; The Whole Council gets all seven.

## Connecting on claude.ai

1. Sign in to claude.ai with your program seat.
2. Create a Project and name it after your department (for example: Customer Ops Agent, Grand Inflation).
3. For each system, click **Add to Claude** on `/start` or in the Field Guide. Claude opens with the connector name and URL already filled in; save it. No OAuth dance, no keys: the session slug in the URL is the whole handshake. (Manual route, same result: Settings, then Connectors, then Add custom connector, and paste the URL.)
4. Repeat for each system in your list.
5. Paste your completed Agent Role Definition into the Project instructions. Design before build: the ARD comes first, always.

**Using Claude managed agents instead?** Same idea, different door. Create a managed agent, and in its Quick Start paste a short brief: the agent's name, its role in one line, and the list of MCP server URLs from your Field Guide (each starter spec in the packet includes a ready-made Quick Start block). When each connector asks for authorization, approve it: the lab's authorization screen auto-approves, because the session URL is already the credential. Then paste the instructions block as the agent's instructions. Everything else in this sheet applies unchanged.
6. Verify: ask the agent to list its tools, then to pull one real record (a ticket, an account, a batch, the helium ledger). If it can do both, you are live.

## Claude Code

`/start` also shows a paste block: one `claude mcp add` line per system. Paste the block into a terminal and everything is connected in about thirty seconds. Same URLs, same world.

## Claude Desktop

Works identically to claude.ai. Same URLs, same connector flow, nothing extra to set up for the lab.

## Managed agents (shared credential vault)

If your platform wraps connectors in a managed-agent credential vault, it will run an authorization step when you add each system. This is automatic: the servers speak OAuth and auto-approve, so the vault completes and stores a credential without any login, and without you pasting a key. The session slug in the URL is still the whole credential; the authorization is just a formality the vault requires. If the vault ever prompts you to *paste* a key, you can leave it blank; the URL is enough.

## Any other platform

MCP is an open standard. Any client that speaks MCP over streamable HTTP connects with the same URLs: another vendor's agent builder, an orchestration framework, or a bare SDK. The servers are stateless JSON-RPC over POST (initialize, tools/list, tools/call), with no auth handshake beyond the URL itself.

## When it does not work

| Symptom | What it means | The fix |
| - | - | - |
| 401 invalid session | Typo in the URL | Re-copy the connector URL from `/start` or the Field Guide rather than retyping the slug |
| 403 department does not have access | Working as designed: that system is not in your charter | You are not missing a permission; you are missing a colleague. The information moves over AirMail, between the agents you build, which is the lesson |
| Connected but no tools | The client cached a failed handshake | Remove the connector entirely and add it again fresh |
| "Authorization failed" in a managed-agent vault | The vault cached an authorization attempt from before OAuth was available, or mid-deploy | Remove the connector and add it again; the authorization now auto-approves. Any "paste a key" prompt can be left blank |
| Tools work, but the world never changes | The story is waiting for you | Press "Advance the story" in the Field Guide. The incident stage additionally requires containment before the story moves on |

Rule of thumb: the URL is the entire configuration. If something is wrong, it is almost always the URL.

# Windows 11 + Ollama installer test (issue #781)

Community test by @Anurag07-crypto, reviewed by the maintainer on 2026-11-05 in https://github.com/ragleap/ragleap-core/issues/781

## What was tested
RagLeap Core installed on Windows 11 with Docker Desktop and the Ollama option, then one PDF ingested and one question answered through the chat API.

## Environment (from the screenshots)
- Windows 11 Pro 25H2, build 26200.9711
- Docker 29.9.2, Docker Compose v5.6.1, Git for Windows 2.54.0, Ollama 0.40.14
- Chat model qwen2.5:3b, embedding model nomic-embed-text (768 dimensions)

## Reported results (test_results.txt)
- Services started and the dashboard opened at localhost:8000/office
- The chat connection test and the embedding connection test passed
- One PDF (pdh.pdf) was ingested: 5 chunks
- The chat API answer returned HTTP 200 and named the source (pdh.pdf)
- The first response was slow; timings were not measured

## Not established
Other Windows versions or hardware. Exact install or response times: the installation recording is about 6 minutes long while the build step on screen reports about 15 minutes, so do not use the recording's length as an install time. Answer accuracy beyond this one PDF and question. Repeated runs, large files or many users. Autonomous actions and approvals (autonomy was off). Security.

## Files
- test_results.txt
- screenshots/
- Three silent screen recordings (installation, dashboard overview, chatbot response) are attached to the release `windows-ollama-781`: https://github.com/ragleap/community-tests/releases/tag/windows-ollama-781

Summary prepared with AI assistance from the contributor's files. The original files are in this folder and in the release.

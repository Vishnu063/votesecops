# Voting application deployment lab: reviewer guide

A multi-service voting application with Docker/Swarm, Kubernetes, Helm, and monitoring configurations.

## Start the review

Explain the vote-to-Redis-to-worker-to-database-to-results path. Preserve original author and license information and show your own infrastructure changes.

| Source | Review focus |\n| --- | --- |\n| [docker-compose.yml](docker-compose.yml) | Build context, runtime configuration, ports, and persistence |\n| [helm/votesecops/Chart.yaml](helm/votesecops/Chart.yaml) | Implementation, assumptions, and operational boundaries |\n| [helm/votesecops/templates/backend.yaml](helm/votesecops/templates/backend.yaml) | Implementation, assumptions, and operational boundaries |\n| [helm/votesecops/templates/db-pvc.yaml](helm/votesecops/templates/db-pvc.yaml) | Implementation, assumptions, and operational boundaries |\n| [helm/votesecops/templates/networkpolicy.yaml](helm/votesecops/templates/networkpolicy.yaml) | Implementation, assumptions, and operational boundaries |\n| [helm/votesecops/templates/web.yaml](helm/votesecops/templates/web.yaml) | Implementation, assumptions, and operational boundaries |

## A useful interview walkthrough

1. State the problem and the specific part you implemented or changed.
2. Open the source above and follow one request, release, or failure from start to finish.
3. Show a reproducible result, including an actual failure and the observation that confirms recovery.
4. Explain one tradeoff and one limitation. Distinguish a local test from a live deployment.

## Evidence and limits

This guide is based on the default-branch source inspected on 16 October 2026. It is a source review, not a fresh deployment or a certification of every feature. Existing CI runs and tests should be checked at the commit being demonstrated. Do not present screenshots, inherited code, planned features, or old README statements as proof of a current deployment.

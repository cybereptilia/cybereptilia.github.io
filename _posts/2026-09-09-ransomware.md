---
layout: post
title: "Ransomware: Why Your Backups Probably Won't Save You"
date: 2026-09-09
---

"Just make sure to have good backups" used to be the reasonable advice in 2015. But now, a decade has passed and the business model has changed. Defenses developed around the encryption event are defending the wrong thing. 

## What changed

**Extorsion moved before encryption.** Attackers extract first and encrypt second. Paying is no longer about recovering important data assets but preventing publication. A perfect restore involves systems do come back and the systems continue functioning but the attacker is still extorting the organization, given the perpetrator is still holding the data.

**Backups became a target.** Perpetrators now strive for backup infrastructure and virtualized environments during the dwell period, given the destruction of the recovery path is what forces payment. A backup server available to production is not necessarily a recovery plan but another target.

**The skill floor collapsed.** Ransomware as a Service split the developer environment into professionals who can build the tooling and affiliates who run or allow intrusions. The associate in your network may not be able to write any malware.

**Some campaigns dropped encryption as a whole.** If the leverage implies publication, encryption becomes optional, and theft-only extortion defeats any control developed to detect mass file modification.

## Why backups fail

Four failure modes are responsible for most of it.

The backups were reachable, because the backup system was able to be authenticated against the same directory the attacker compromised.

The restore was never really tested. A backup that has never been restored becomes an assumption, not a control.

The restore timing exceeded the tolerable downtime. If the recovery objective is 24 hours and a full restore takes twelve days, the backups do exist but the organization would still fail.

The restore reintroduced the attacker, given backups keep whatever contents were on the system, including any persistence installed weeks earlier.

## What actually reduces impact

To keep at least one inmutable copy, unable to be changed within the retention period, and one that is unavailable to production credentials. Also, run the restore, time it, and compare the amount of time to what the business can tolerate. Network segmentation, given most of the damage occurs during lateral movement instead of encryption. The implementation of phishing-resistant MFA on all remote access is key, because initial permission to the system remains credential based. Enforcement of least-privilege to evade the accumulation of access control, in order to mitigate the blast radius.

## The point

Ransomware is a problem that business continuity is responsible for, and it also involves malware. The organizations able to recover successfully are not the ones with the finest endpoint detection. They happen to be entities that measured their recovery time, kept a copy the attacker was not able to obtain, and had already planned on the next steps.

The work occurs prior to the incident or it does not happen at all.

# jira-timelog

Command-line Time Logger for Jira

## WARNING

***PLEASE NOTE:*** This was a learning project and is **NOT** actively maintained.

## Usage

First setup the necessary environment variables: JTL_USERNAME and JTL_PASS. You can do this using:

```bash
export JTL_USERNAME=my.cool.username
export JTL_PASS=mysecretpass
```

### Commands

#### List current issues

```bash
jtl
```

or

```bash
jtl list
```

#### List of hours worked

The command is:

```bash
jtl logs [options] <date>
```

Examples:

```bash
jtl logs 2018-09-04
```

to filter by project use:

```bash
jtl logs --project=INT 2018-09-04
```

#### Log hours worked

The command is:

```bash
jtl log [options] <issueId> <time> [message]
```

Examples:

Normal logging:

```bash
jtl log INT-123 1h
```

Logging with a different message:

```bash
jtl log INT-123 1h "Wow a cool message"
```

Logging with a different date than today:

```bash
jtl log --date=2018-08-28 INT-123 1h
```

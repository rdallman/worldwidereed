---
ShowReadingTime: false
---

# Reed Allman

<hire@reed.pizza> · [reed.pizza]

-------------------------------------------------------------------


I have lots of experience with building message queueing and job processing
systems, coding, configuring and operating docker, Golang and AWS at scale,
stewarding open source projects that have live production environments, and
working in mixed remote teams spread around the globe.  I try to build systems
that are fast, easy to understand and obviously correct, and sometimes it even
happens.

### Labor

**Dec 2019-Current, Self Employed**

  *  Available on a contract basis for cloud, cryptocurrency, security,
     distributed systems, and static analysis work
  *  COVID-19 survivor (so far)
  *  Underwent intensive pizza research and development

**May 2017-Dec 2019, Principal Member of Technical Staff, Oracle**

  *  Core contributor on [Fn], an open source Functions as a Service (FaaS)
     product that leverages Docker to run any container in a FaaS fashion.
     Primarily focused on load balancing, scalability, task execution, storage
     and messaging.
  *  Involved in building out a hosted version of [Fn] on Oracle's cloud.
  *  Re-architected task running agent in order to reduce start latencies,
     making it possible for tasks to wait on existing containers of a function
     kind to become available to run while a new container may be spawned,
     where previously most of those tasks would time out. This also brought
     down the number of containers launched during spikes by a painfully
     large, unknown factor (early days!).
  *  Led API 2.0 redesign effort, after spending many months working with our
     v1 API we discovered it was unintuitive when adding hooks into various
     services to trigger tasks: an API gateway, an s3-like store, etc. This
     led to an effort to rework our API to allow functions to be their own
     entity, and to have a one-to-many relationship with triggers (as is
     industry-standard for FaaS).
  *  Led effort to separate API nodes from task running nodes. We needed a way
     to separate these in order to put task running nodes in a separate network
     from API nodes, where API nodes are a touch point for users to deploy and
     manage functions on, but task running nodes operate on a separate network.
  *  Led effort to instrument all code with [OpenCensus], a distributed
     tracing and statistics library with plugs for many backends. Used these
     to reduce latency in our critical path more than once; reduced
     allocations, removed docker logging, batched writes, among others.
  *  Presented talks at Devoxx, GoSF, and various meetups about Fn. Wrote a
     number of blog posts for [Fn medium]. Helped users debug their computers
     in Slack. Reviewed a zillion Pull Requests. Wore a T-shirt bearing the
     Fn logo once a week around SF to fulfill Peter Thiel's prophecy.

**May 2014-April 2017, Senior Backend Engineer, [Iron.io]**

  *  Co-built a strongly consistent, distributed key-value store on top of RocksDB.
     Built distributed transactions, node membership, dynamic load balancing,
     automagic sharding, and automagic rebalancing. Based on [Viewstamped
     Replication], [Gossip protocol], and [Two-phase commit], among others.
  *  Co-built IronMQ v3, a distributed message queue system on top of that,
     specifically for performance + persistence for processing [delayed] jobs,
     [it scales].  Processed tens of billions of messages per month.
  *  Built authentication service on top of said distributed key-value store,
     as well (much easier than the queue).
  *  Increased cluster utilization from <40% to >80% by building a custom
     autoscaler for job processing servers. Saved lots of $$$ and zzz,
     didn't have to launch servers by hand anymore.
  *  Migrated job runner from Ruby to Go. Decreased p99 task start time 100x,
     p75 by 30x by simplifying API and intelligent, probabilistic queue
     polling. Eliminated issues of jobs getting stuck in queue.
  *  Migrated infrastructure from upstart scripts and binaries to CoreOS,
     systemd and Docker. Setup push button releases for all products.
  *  Wrestled with Linux. Battled Docker. Wrote a lot of Go code. Ran a lot of
     Go code. Contributed to RocksDB, CoreOS. Presented talks at meetups and
     conferences about IronMQ. Wrote blog posts.

**May 2013-May 2014, Undergraduate Research Assistant, Auburn University** 

  *  Built refactoring tools. Funded by Google to work on refactoring Go. C:
     [OpenRefactory] Go: [godoctor]
  *  Built a statement level control flow graph for Go source code and used
     that to do data flow analyses.
  *  Constructed a pretty awesome testing infrastructure to test our tool on
     all the Go source I could find (4.5M lines).
  *  Developed the CLI, Sublime Text plugin, Vim plugin and JSON protocol for
     C and Go refactoring tools.

### Education

**Bachelor of Software Engineering, Auburn University, 2010-2014**

  *  Minor in Business-Engineering-Technology (engineering entrepreneurship)

### Contributions

  *  I dabble in open source: [github]
  *  Sometimes I write: [medium]
  *  Occasionally I can be convinced to stand in front of people: [speakerdeck]
  *  Former co-organizer of [GoSF] and [RocksDB] meetups

### Human Bits

  * Can solve 3x3 Rubik's cube in 15s
  * Can stand on my head for a minute
  * Can send certain boulders on certain days
  * Can do Sunday NYT crossword some weeks
  * Can make a pretty sick pizza
  * Can win fantasy baseball or football leagues
  * Can travel to a 'stan and make it back alive
  * Cannot figure out whether the top keeps spinning at the end of Inception

[Viewstamped Replication]:http://pmg.csail.mit.edu/papers/vr-revisited.pdf
[Gossip protocol]:https://www.cs.cornell.edu/home/rvr/papers/GossipFD.pdf
[Two-phase commit]:https://en.wikipedia.org/wiki/Two-phase_commit_protocol
[it scales]:https://www.iron.io/1m-msgsec-ironmqv3-hits-dos-commas/
[github]:https://github.com/rdallman
[godoctor]:https://github.com/godoctor/godoctor
[Iron.io]:https://iron.io
[OpenRefactory]:https://www.openrefactory.com
[reed.pizza]:https://reed.pizza
[speakerdeck]:https://speakerdeck.com/rdallman
[GoSF]:https://www.meetup.com/golangsf
[RocksDB]:https://www.meetup.com/RocksDB
[medium]: https://medium.com/@rdallman10
[Fn]:https://github.com/fnproject/fn
[OpenCensus]:https://opencensus.io
[Fn medium]:https://medium.com/fnproject

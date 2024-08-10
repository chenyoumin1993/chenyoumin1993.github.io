---
layout: research
title: Research
permalink: /research/
---

<div style="text-align: justify">
With the burgeoning demand for real-time data processing, the imperative to construct large-scale memory storage systems 
has become paramount. In light of this, the data center infrastructure is actively exploring innovative storage and network 
technologies, exemplified by byte-addressable non-volatile memory from Intel (e.g., Optane) and Samsung (CMM-H), and high-speed 
RDMA interconnections. 
</div>

<div style="text-align: justify; margin-bottom: 20px">
My research focus on developing efficient and robust next-generation storage systems utilizing these 
new hardware devices. I follow three fundamental design principles – CPU-awareness, device-awareness, and workload-awareness – 
essential for achieving optimal device bandwidth utilization, minimal CPU overhead, and predictable high performance. 
</div>

<h2>Networked Memory Architecture</h2>

2017 - 2020

As the storage and network technologies evolve rapidly, the CPU performance remains comparatively
stagnant as Moore's law slows in the past years. Due to this reason, the CPU running with the
heavy-weight storage software can easily become the bottleneck. We tackle this problem from various aspects.
In the OS level, we break the common wisdom of strict separation of user and kernel spaces by introducing the
kernel-userspace collaboration architecture ([Kuco[FAST'21]](/papers/fast21-kucofs.pdf)), which enables direct storage access with minimal software
overhead. We also extend the use of NVM in distributed environment by introducing RDMA-enabled
persistent distributed shared memory (or pDSM) to eliminate redundant memory copies ([Octopus[USENIX ATC'17, TOS'20]](/papers/atc17-octopus.pdf)).


<h2>CPU-efficient IO Engine</h2>

2010 - 2024

Purely reducing the overhead of storage software is still not enough; system designers must be
also device-aware since the emerging hardware typically exhibits bizarre performance behavior. For example,
NVM has asymmetric read/write performance, device-level IO amplification, and performance variability;
RDMA shows limited scalability due to the device-level cache thrashing. In this context, I have designed an
asynchronous IO framework to hide NVM's high access latency ([EasyIO[EuroSys'24]](/papers/eurosys24-easyio.pdf)), a key-value store that uses compacted
log to mitigate the IO amplification ([FlatStore[ASPLOS'20]](/papers/asplos20-flatstore.pdf)), 
and an RPC system to enable RDMA to work at a larger scale ([ScaleRPC[EuroSys'19]](/papers/eurosys19-scalerpc.pdf)).

<h2>Low Tail Latency Concurrency Control</h2>

2010 - 2024

Apart from seeking higher throughput and lower latency, datacenter applications also
require their performance to be predictable (often defined as 99th or 99.9th percentile latencies). Latency
variability can arise for many reasons, including sharing resources (e.g., CPU cores, caches, memory bandwidth,
etc.), background activities, queuing, and others. In the past years, we have witnessed an active line of
research work that improves performance predictability at different layers, but they ignore that fact that the
workload is another source of incurring latency spikes due to request conflicts. Here, I take a much deeper dive
to the concurrency protocol design and introduced coordinated concurrency control ([uTree[VLDB'20]](/papers/vldb20-utree.pdf)) and pessimistic
locking and opportunistic reading ([Plor[SIGMOD'22]](/papers/sigmod22plor.pdf)) with the workload-aware principle in mind.

<!-- <div class="home" style="font-size: 0.9em;">
    <ul class="responsive-table" style="margin-left: 0">
        <li class="table-row table-row-assignment">
            <div class="col col-3">Networked Memory Architecture</div>
            <div class="col col-2">2017-2020</div>
            <div class="col col-4">As the storage and network technologies evolve rapidly, the CPU performance remains comparatively
                stagnant as Moore's law slows in the past years. Due to this reason, the CPU running with the
                heavy-weight storage software can easily become the bottleneck. We tackle this problem from various aspects.
                In the OS level, we break the common wisdom of strict separation of user and kernel spaces by introducing the
                kernel-userspace collaboration architecture (Kuco[FAST'21]), which enables direct storage access with minimal software
                overhead. We also extend the use of NVM in distributed environment by introducing RDMA-enabled
                persistent distributed shared memory (or pDSM) to eliminate redundant memory copies (Octopus[USENIX ATC'17, TOS'20]).</div>
        </li>
        <li class="table-row table-row-exam">
            <div class="col col-3">CPU-efficient IO Engine</div>
            <div class="col col-2">2020-2024</div>
            <div class="col col-4">Purely reducing the overhead of storage software is still not enough; system designers must be
                also device-aware since the emerging hardware typically exhibits bizarre performance behavior. For example,
                NVM has asymmetric read/write performance, device-level IO amplification, and performance variability;
                RDMA shows limited scalability due to the device-level cache thrashing. In this context, I have designed an
                asynchronous IO framework to hide NVM's high access latency (EasyIO[EuroSys'24]), a key-value store that uses compacted
                log to mitigate the IO amplification (FlatStore[ASPLOS'20]), and an RPC system to enable RDMA to work at a larger scale (ScaleRPC[EuroSys'19]).</div>
        </li>
        <li class="table-row table-row-due">
            <div class="col col-3">Low Tail Latency Concurrency Control</div>
            <div class="col col-2">2020-2022</div>
            <div class="col col-4">Apart from seeking higher throughput and lower latency, datacenter applications also
                require their performance to be predictable (often defined as 99th or 99.9th percentile latencies). Latency
                variability can arise for many reasons, including sharing resources (e.g., CPU cores, caches, memory bandwidth,
                etc.), background activities, queuing, and others. In the past years, we have witnessed an active line of
                research work that improves performance predictability at different layers, but they ignore that fact that the
                workload is another source of incurring latency spikes due to request conflicts. Here, I take a much deeper dive
                to the concurrency protocol design and introduced coordinated concurrency control (uTree[VLDB'20]) and pessimistic
                locking and opportunistic reading (Plor[SIGMOD'22]) with the workload-aware principle in mind.</div>
        </li>
    </ul>
</div> -->
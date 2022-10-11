# NDC Sydney 2022

## Securing your .NET application software supply-chain

With our complete software development process becoming more complex we also got a lot more security problems to deal with. What starts with code and ends with releasing/deploying software is also being referred at as the software-supply chain.

The software supply-chain consists of a lot of moving parts. Each of them facing their own security risks starting from access to source code, compromised third-party libraries and tools, or even hacked build servers. For example with SolarWinds the compromised build server added malicious functionality to the end product used by their customers. And a tool called CodeCov had their upload script compromised which resulted in it stealing all used access-keys.

In this session we'll get hands-on with securing a .NET application it's supply chain and look how we can limit the security risks in all the different area's. We're going to use the guidance of Google's SLSA and using concepts like Software Bill Of Materials (SBOM).

https://github.com/nielstanis/ndcsydney2022-supplychain

## Sandboxing .NET assemblies for fun, profit and of course security!

In our current way of developing .NET applications we rely a lot on third-party libraries developed by others. This of course has a lot of benefits from productivity perspective because there is no need to write needed functionality from scratch.

But by using in a third-party library you also pull in it's issues and possibly security problems that are found over time. What does the library do? And what type of other libraries and/or functionality does it rely on? What do the projects/people behind it do for security?

If we develop a .NET application using external libraries can we improve our security posture? Other new technologies like WebAssembly introduced a concept of nano-process, which allows the developer to limit the capabilities available for an external module by creating a restricted sandbox for it. Could we maybe do the same in .NET? In the old days we could use AppDomains and Code-Access Security (CAS) to achieve that, but with the introduction .NET Core there only is a single AppDomain and CAS has been deprecated.

Luckily with .NET Core we did get more internals exposed on AssemblyLoadContext and in this session we're going to create a sandbox using that. A restricted sandbox that limits the functionality available that will improve the security posture of our application!

https://github.com/nielstanis/ndcsydney2022-sandbox

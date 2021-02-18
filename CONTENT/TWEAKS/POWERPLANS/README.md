## Power plans

### The importance of a good power plan.
The power plans are a feature provided by Microsoft to set specific settings for your processor, etc...

<details><summary>Findings and Analysis</summary>
The power plans can be used to conserve power for laptops, but this is not why I made this topic. A good power plan can improve your performances in games or even in common tasks.
A lot of people in the tweaking community provide power plans, but which one is the best? Can we see any difference between them?

In this section I will provide some tests to see which power plan is the best from those that were tested, but you can do your own power plan with [PowerSettingsExplorer](https://forums.guru3d.com/threads/windows-power-plan-settings-explorer-utility.416058/).
<hr>

**[Mouse tester](https://www.overclock.net/threads/mousetester-software.1535687/)**

This program was made with the goal to obtain data about your mouse. This is a useful program to check if your mouse is stable at a given polling rate.
- Adamx's: [30hertz variation]
![](https://github.com/littleunixcorn/Unicorns/blob/main/assets/images/mousetester/adamx.png?raw=true)
- Calypto's (idle disabled): [40hertz variation]
![](https://github.com/littleunixcorn/Unicorns/blob/main/assets/images/mousetester/calypto_idle_disabled.png?raw=true)
- ggOS (v2): [15hertz variation and a spike at ~30]
![](https://github.com/littleunixcorn/Unicorns/blob/main/assets/images/mousetester/ggos_v2.png?raw=true)
- High Performance Default: [30hertz variation and a spike at ~50]
![](https://github.com/littleunixcorn/Unicorns/blob/main/assets/images/mousetester/high_performance_default.png?raw=true)
- Muren's (idle disabled): [10hertz variation and a lot of spikes]
![](https://github.com/littleunixcorn/Unicorns/blob/main/assets/images/mousetester/muren_idle_disabled.png?raw=true)
- Muren's (idle enabled): [~25hertz variation and two spikes at ~60hertz]
![](https://github.com/littleunixcorn/Unicorns/blob/main/assets/images/mousetester/muren_idle_enabled.png?raw=true)
- My power plan: [~20hertz variation]
![](https://github.com/littleunixcorn/Unicorns/blob/main/assets/images/mousetester/unicorn.png?raw=true)

**[Latencymon](https://resplendence.com/latencymon)**

This program was designed to prevent audio stutters, but it is commonly used by tweakers as a latency tester program. Keep in mind that the values are in microseconds (`1s = 1000000us`).
- Adamx's:
![](https://github.com/littleunixcorn/Unicorns/blob/main/assets/images/latencymon/adamx.png?raw=true)
- Calypto's (idle disabled):
![](https://github.com/littleunixcorn/Unicorns/blob/main/assets/images/latencymon/calypto_idle_disabled.png?raw=true)
- ggOS (v2):
![](https://github.com/littleunixcorn/Unicorns/blob/main/assets/images/latencymon/ggos_v2.png?raw=true)
- High Performance Default:
![](https://github.com/littleunixcorn/Unicorns/blob/main/assets/images/latencymon/high_performance_default.png?raw=true)
- Muren's (idle disabled):
![](https://github.com/littleunixcorn/Unicorns/blob/main/assets/images/latencymon/muren_idle_disabled.png?raw=true)
- Muren's (idle enabled):
![](https://github.com/littleunixcorn/Unicorns/blob/main/assets/images/latencymon/muren_idle_enabled.png?raw=true)
- My power plan:
![](https://github.com/littleunixcorn/Unicorns/blob/main/assets/images/latencymon/unicorn.png?raw=true)

<hr>

As you can see, a power plan is not a thing to ignore. This can help your polling rate be more stable, reduce your latency and improve your fps (I will upload some benchmarks soon).
If you have free time, you can even try to disable the `Power` service which is responsible for the use of power plans.
I would be happy if you can bring me some feedbacks, or even your own power plan(s) !
</details>

# Introduction to Efabless Caravel
Caravel is a template SoC for Efabless Open MPW and chipIgnite shuttles based on the Sky130 node from SkyWater Technologies.
* [Caravel User Project](https://caravel-user-project.readthedocs.io/en/latest/#caravel-user-project)
* [Efabless Caravel “harness” SoC](https://caravel-harness.readthedocs.io/en/latest/#efabless-caravel-harness-soc)

<img src="https://user-images.githubusercontent.com/11850122/214560743-cbad9de0-db4c-4ab1-9a0a-cc52d51191dd.jpg" width=120%>

## Caravel Lab Purpose
* Integrate a custom RTL design to Caravel SoC
* Go through overall Caravel flow and ready to [MPW submission](https://efabless.com/open_shuttle_program)

## Caravel Lab Prerequisites
* Ubuntu 20.04+
* Installed Docker packages
* Icarus Verilog [version 12.0](https://bleyer.org/icarus/)
* Caravel user project sources with [tag mpw-8c](https://github.com/efabless/caravel_user_project/tree/mpw-8c)

## 1. Custom RTL design
A GCD RTL design example was verified under Icarus Verilog version 12.0. The the following timing diagram shows GCD(10312050, 29460792) = 138.

<img src="https://user-images.githubusercontent.com/11850122/214568278-017816f2-8450-483e-878f-8cbccd79d248.png" width=100%>

    $ iverilog design.v testbench.v  && vvp a.out
    VCD info: dumpfile dump.vcd opened for output.
                 Result is correct:  GCD(  10312050,  29460792) -->: Expected =        138; Actual Result =        138
                 Result is correct:  GCD(1993627629,1177417612) -->: Expected =          7; Actual Result =          7
                 Result is correct:  GCD(2097015289,3812041926) -->: Expected =          1; Actual Result =          1
                 Result is correct:  GCD(1924134885,3151131255) -->: Expected =        135; Actual Result =        135
                 Result is correct:  GCD( 992211318, 512609597) -->: Expected =          1; Actual Result =          1
    testbench.v:101: $stop called at 609 (1s)
    ** VVP Stop(0) **
    ** Flushing output streams.
    ** Current simulation time is 609 ticks.

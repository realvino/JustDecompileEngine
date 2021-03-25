# JustDecompile Engine

This is the engine of the popular .NET decompiler [JustDecompile](https://www.telerik.com/products/decompiler.aspx). C# is the only programming language used.

Copyright (c) 2011 - 2018 Telerik ЕAD

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

     http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.


## Getting Started

- Clone the repository and open JustDecompileEngine.sln in Microsoft (r) Visual Studio (r).
- Set your startup project to ConsoleRunner.
- Enjoy

See this [getting started](https://developer.telerik.com/featured/a-look-at-the-open-source-justdecompile-engine/) post for more info. 

## Working with JustDecompile Engine

JustDecompile UI remains private at this time. JustDecompile, however, has rich console functionality and that has been opensourced here.
One can use the console project generation feature to see the results of the changes made to the engine. The ConsoleRunner project
is a console app that exposes that functionality and makes testing easy. When started it prints out all the available commands and switches. 

## How to Contribute to JustDecompile Engine

We encourage and support an active, healthy community that accepts contributions from the public. We'd like you to be a part of that community.

Before submitting a pull request, please, read and sign the [Contributors License Agreement](https://docs.google.com/forms/d/e/1FAIpQLSdjOagw622VxQLrWOsnsLoqvncwJ_DfPmC9hyiYci8iaVWONQ/viewform)

## How to Contribute to JustDecompile


[Feature Suggestions](https://feedback.telerik.com/Project/189)

[Bug Reports / Discussion](https://www.telerik.com/forums/justdecompile/general-discussions)

## Related

The [JustDecompile Plugins](https://github.com/telerik/justdecompile-plugins) are also available on GitHub under various open source licenses. 

public class App
    {
        public static void Main(string[] args)
        {
            string[] testArgs = { @"/target:C:\Users\vinor\Desktop\DemoApp\MaterialDesignDemo.exe", @"/out", @"C:\Users\vinor\Desktop\DemoApp\Source" };
            GeneratorProjectInfo generatorProjectInfo = CommandLineManager.Parse(testArgs);
            CmdShell shell = new CmdShell();
            shell.Run(generatorProjectInfo);
        }
    }

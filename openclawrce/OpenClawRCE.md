Command Execution Vulnerability in OpenClaw v2026.3.13

Discoverer: Terry Tian

Credits: westsec Security Team!

1.  Introduction to Vulnerable Project and Affected Version

    Project Overview

Open-source Project:
[openclaw/openclaw](https://github.com/openclaw/openclaw)

Project Repository:

https://github.com/openclaw/openclaw

Official Demo/Blog URL: [https://openclaw.ai](https://www.foxcms.cn/)

Project Description: \"Your own personal AI assistant. Any OS. Any
Platform. The lobster way.\"

Affected Version

Version Number: v2026.3.13 (Latest stable release)

Release Page:
[https://github.com/openclaw/openclaw/releases](https://gitee.com/qianfox/foxcms.git)

2.  Vulnerability Environment Construction: Ollama + Qwen Large Model

Launch the Qwen large model, as shown in the figure:

ollama run qwen2.5:7b

![](images/media/image1.png){width="5.7659722222222225in"
height="2.3027777777777776in"}

Launch the OpenClaw gateway, as shown in the figure:

openclaw gateway \--port 18789 \--verbose

![](images/media/image2.png){width="5.759027777777778in"
height="3.3090277777777777in"}

3.  Vulnerability Proof Process

The vulnerable software version is: OpenClaw 2026.3.13, as shown in the
figure:

![](images/media/image3.png){width="5.766666666666667in"
height="1.4506944444444445in"}

Functional points and specific processes of the software vulnerability,
as shown in the figure:Log in to the background, click Configuration,
Communication, Appearance and Settings, AI & Agents, Infrastructure or
Automation, then click Open --- the system will directly launch the
command console by default, as shown in the figure:

![无标题](images/media/image4.png){width="5.759722222222222in"
height="3.2402777777777776in"}

![无标题](images/media/image5.png){width="5.759722222222222in"
height="3.2402777777777776in"}

![无标题](images/media/image6.png){width="5.759722222222222in"
height="3.2402777777777776in"}

![无标题](images/media/image7.png){width="5.759722222222222in"
height="3.2402777777777776in"}

![无标题](images/media/image8.png){width="5.759722222222222in"
height="3.2402777777777776in"}

![无标题](images/media/image9.png){width="5.759722222222222in"
height="3.2402777777777776in"}

![](images/media/image10.png){width="5.759722222222222in"
height="3.06875in"}

At this point, system commands can be executed directly in the command
console, as shown in the figure:

![](images/media/image11.png){width="5.759722222222222in"
height="3.0597222222222222in"}

Remediation Recommendations: Direct access to the command console is
strictly prohibited. Restrict operational privileges to the minimum
necessary---only allow opening, editing, and saving the required
configuration files.

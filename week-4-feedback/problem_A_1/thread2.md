# THREAD: Infrastructure & Security

# PARTICIPANTS: Requirements Engineer (RE), Sarah Chalke (IT Director)

# DATE: Oct 14, 202X

# SUBJECT: Re: API Access and Server Specs

Requirements Engineer:
Hi Sarah,
Following up on our call. We are looking into cloud hosting (AWS) for the ParkSmart user database to handle the mobile app traffic.
We also need to know about the existing barrier gates—can we control them via an API?

Sarah Chalke:
Whoa, hold on.
We absolutely cannot host student data on AWS. The university has a strict policy that all Personally Identifiable Information (PII)—which includes student names and license plates—must be hosted On-Premise in our basement server room.
We have a Windows Server 2019 rack you can use.
The only thing that can go to the cloud is the credit card processing (we use Stripe).

Requirements Engineer:
Okay, that is a major constraint. We will design for On-Premise PII storage.
What about the internet connection at the parking lots? We need that for the cameras to talk to the local server.

Sarah Chalke:
The lots are on the edge of campus. The Wi-Fi is spotty at best.
You’ll need to hardwire everything via Ethernet.
Also, regarding the gates—they are "GateMaster 2000" models installed in 2005. They don't have an API. They just have a dry contact relay (a physical wire pair) that needs to be shorted to open. You'll need a hardware controller to trigger them.

Requirements Engineer:
Got it. Legacy hardware integration required.

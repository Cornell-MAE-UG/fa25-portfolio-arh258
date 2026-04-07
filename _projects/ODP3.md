---
layout: project
title: Sorry Little Fly - ODP
description: Prototyping a mechanical device for MAE2250 in order to address the problem of the invasive Spotted Lantern Fly species in NY, particularly in upstate NY vineyards.
technologies: []
image: /assets/images/SquashedSLF.png

---
<div style="display:flex; align-items:center; gap:40px; margin:30px 0;">



  <div>
    <h2 style="margin-top:0;">Table of Contents</h2>
    <ul>
      <li><a href="#client-pitch">Client Pitch</a></li>
      <li><a href="#functional-prototype">Functional Prototype</a></li>
    </ul>
  </div>

</div>

---

## <span style="background-color:#97bfcc; padding:6px 14px; border-radius:8px;">Client Pitch</span> {#client-pitch}

Download this [Client Proposal]({{ "/assets/SLF/ClientProp.pdf" | relative_url }}) in PDF format.

**Team:** Sorry Little Fly  
**Client(s):** Cornell CALS Extension / E&J Gallo Winery / National Grape  

## Problem statement
Spotted lanternflies reproduce rapidly; each female lays 3 egg masses of 30–60 eggs, allowing populations to explode in a single season. SLFs feed on sap, weakening vines, reducing cold hardiness, and potentially killing plants. Current removal methods are labor-intensive, inconsistent, and risk damaging vines. 

**Impact:** Destroying egg masses reduces SLF reproduction, lowering seasonal infestations and protecting yield and vine health. A plant-safe, scalable tool could be used across vineyards and other sites, targeting the root source of infestations and increasing overall population control.

### Concept A (primary): Radial Compression Mechanism
**What it is:**  
A handheld circular frame fits around the vine, positioning radially arranged claws over each egg mass. A manual lever converts input force into uniform inward radial compression, crushing and destroying eggs without damaging the plant.

**How it would be used:**  
- Place the open circular frame around the egg mass so the claws align properly.  
- Pull the lever, causing the claws to move inward and apply compressive force on egg cluster  
- Release the lever and reposition the device on the next egg mass.  
- Repeat until all visible egg masses are treated in the vine section.

**Why it’s better than the status quo:**  
- Provides controlled, consistent crushing force versus variable scraping.  
- Distributes load radially, reducing bark damage and minimizing vine injury.  
- Chemical-free, repeatable across workers, and faster per egg mass than manual scraping.

**End-of-semester proof-of-concept:**  
Build a scaled mechanical prototype with 3–4 arms and lever linkage. Test crushing force on mock egg masses while measuring pressure on a vine analog to ensure plant-safe operation.

**Key risks / unknowns**
 - Force vs. bark damage; excessive force could harm vines, experimentally determine safe range  
 - Incomplete egg destruction; may not properly prevent reproduction, validate using mock materials  
 - Field usability; operating the tool may be slow or ergonomically challenging, test timed trials and ergonomics

**Questions for the client**
- Is crushing the egg mass sufficient, or must it be fully removed and disposed of? *Decision affected:* Required force and containment design  
- If crushing is sufficient, how much force is required to reliably destroy eggs? *Decision affected:* Feasibility of lever mechanism and force calibration  
- How tall are average grapevines, and can an average worker reach the required height? *Decision affected:* Frame size and tool adjustability  
- Where are egg clusters most commonly located on a grapevine? *Decision affected:* Arm spacing and tool positioning

## References

- Ohio Dept. of Agriculture, “Spotted Lanternfly Best Management Practices.” http://agri.ohio.gov/divisions/plant-health/invasive-pests/slf-bmp  
- Penn State Extension, “What should you do with spotted lanternfly egg masses?” https://extension.psu.edu/what-should-you-do-with-spotted-lanternfly-egg-masses

___

## <center><span style="background-color:#97bfcc; padding:6px 14px; border-radius:8px;">Functional Prototype</span></center> {#functional-prototype}

The functional prototype was built to test whether the device could successfully compress and destroy spotted lanternfly egg masses in a controlled and repeatable way.

### Design Documentation:
The primary components consist of RPL printed parts, including a small spur gear, large spur gear, five blades, a base plate, and a housing. Additional purchased components from McMaster include a pulley (Part #6284K51) with a 1.5-inch outer diameter and a 0.25-inch inner diameter; the inner diameter must be sanded during fabrication to properly fit onto the shaft. An aluminum rod (Part #8974K22), measuring 1 foot in length with a 0.25-inch diameter, is also used and must be cut in half using a bandsaw. From the Taylor Design Lab, twine is incorporated into the design. For assembly, five M3 x 6 mm screws with washers are used to secure the  gear mechanism, along with various lengths of M3 screws to fasten the housing.

##### Assembly:
*Main Assembly:*
  Align fins and gear, screw into baseplate using M3x6mm screws & washers. Sand touching components if needed for smoother movement. Align top & bottom halves of housing, put baseplate/iris assembly on top and screw in using longer screws

*Rod Assembly:*
  Cut Rod down to size. Glue small spur gear onto aluminum rod and slide through housing’s hole. Use superglue/hotglue. Glue pulley onto other side of aluminum rod (underside of housing assembly). Attach twine to pulley using glue & rotate 

##### Sketches
<div style="display: grid; grid-template-columns: 1fr 1fr; gap: 10px; max-width: 800px; margin: auto;">
  <img src="{{ '/assets/images/SLF/MAE 2250-4.jpg' | relative_url }}" style="width:100%;">
  <img src="{{ '/assets/images/SLF/MAE 2250-5.jpg' | relative_url }}" style="width:100%;">
  <img src="{{ '/assets/images/SLF/MAE 2250-6.jpg' | relative_url }}" style="width:100%;">
  <img src="{{ '/assets/images/SLF/MAE 2250-7.jpg' | relative_url }}" style="width:100%;">
</div>

### Design Tests
***1. Force Required Test:***
- *How it was tested:*
  In order to quantify the force required to operate the radial compression mechanism, a spring force gauge was attached directly to the pulley system used to actuate the device. The gauge was aligned with the direction of motion to ensure accurate force readings during operation. Trials were conducted by gradually applying force to both open and close the mechanism while recording the peak force required to reach the fully open and fully closed positions. Multiple trials were performed to ensure consistency and reduce experimental error, and the results were averaged to obtain representative force values. This testing allowed us to evaluate the usability of the mechanism and determine whether the required force falls within an acceptable range for practical operation.
- *What happened:*
  From testing, we found that the mechanism required approximately 5–7 N of force to open and 10–12 N to fully close. In terms of usability, these force levels are relatively low and fall well within the range of what a user can comfortably apply by hand. For comparison, everyday actions such as pressing a standard button or pulling a small drawer typically require forces on the order of 5–15 N, suggesting that the mechanism is not physically demanding to operate. However, the higher force required for closing may indicate inefficiencies in the design, such as friction losses in the pulley system or misalignment of moving parts.

<div style="display:grid; grid-template-columns:1fr 1fr; gap:12px; max-width:800px; margin:auto;">
  <img src="{{ '/assets/images/SLF/Force-Close.png' | relative_url }}" style="width:100%;">
  <img src="{{ '/assets/images/SLF/Force-Open.png' | relative_url }}" style="width:100%;">
</div>

- *Design Changes:*
  To improve the performance and reliability of the mechanism, several design modifications can be implemented. First, the pinion gear casing should be redesigned to fully encase the gear, ensuring proper alignment at all times and preventing any possibility of tooth disengagement during operation. Additionally, incorporating bushings or bearings at rotating joints would help reduce friction while also maintaining proper shaft alignment, leading to smoother motion. Finally, applying lubrication to the gears and tooth slots can further minimize friction losses, improving overall efficiency and reducing the force required to operate the mechanism.


***2. Egg Mass Removal Effectiveness***
- *How it was tested:*
  We created a physical model of a grape vine using flexible stems to replicate the compliance and geometry of real vine branches. A mock egg mass was created using paper towels, glue and water to create a sudo-”paper-maché”. Paper-Maché is fibrous & a semi-rigid material that adheres to surfaces and resists compression, similar to the protective coating of spotted lantern fly egg masses. The paper-maché balls were then attached along the surface of the vine to simulate spotted lanternfly egg masses. This approach was effective because it captured the radial geometry of the vine, requiring our mechanism to interact with a curved surface rather than a flat one. Additionally, gluing the paper balls onto the vine approximated the adhesion of real egg masses, allowing us to test the amount and type of force needed to scrape them off. In reality, egg masses are often clustered and randomly distributed, which we replicated by placing the paper balls in irregular patterns along the vine. This ensured that our testing environment reflected the variability and accessibility challenges present in real vineyard conditions. 
- *What happened:*
  The radial compression mechanism was able to successfully apply force to the simulated egg masses and effectively scrape them from the vine model. However, during testing, we observed that the paper surface of the model vine tore along with the egg masses. This behavior is likely due to the relatively low strength and tear resistance of the paper compared to real grape vine bark. In practice, grape vine surfaces are more durable and would be less likely to fail under the same loading conditions. As a result, this test likely represents a conservative case, and in real-world conditions, the mechanism would be expected to remove egg masses without damaging the vine surface.

<div style="display:grid; grid-template-columns:1fr 1fr; gap:12px; max-width:800px; margin:auto;">
  <img src="{{ '/assets/images/SLF/MockTree1.png' | relative_url }}" style="width:100%;">
  <img src="{{ '/assets/images/SLF/MockTree2.png' | relative_url }}" style="width:100%;">
</div>

- *Design Changes:*
  We plan to modify the scraping interface by incorporating a slightly sharper or textured edge to improve removal efficiency at lower applied forces. Additionally, we may introduce a compliant element, such as a spring or flexible pad, to maintain consistent contact with the vine surface despite slight misalignment. This is motivated by observations during testing where the blades did not maintain full contact with the model grape vine at certain points. Finally, we may implement a centering guide to better align the mechanism with the vine, improving consistency and repeatability across trials.

***3. Repeated Use***
- *How it was tested:*
  The device is repeatedly radially opened and closed via the pulley mechanism attached to the gear and shaft. This is a necessary trial because we wanted to ensure that the device will not fail after repeated usage due to component connections, fragile pieces, or motions that require very specific force inputs that cannot be accurately replicated over time. To accomplish a thorough testing and analysis of these threats, we repeated our input force induced motion 20 times while pulling in a specifically horizontal plane. We then repeated 10 more cycle tests where the input force was angled slightly upwards and another 10 where the input force angle was slightly downwards. 
- *What Happened:*
  After the 20 trials, we noticed that the radial motioned piece behaved consistently and there were no issues that emerged after repeated usage of the device with that particular component. This is something that we anticipated being problematic, and initially was, but was fixed with the implementation of washers and screws to make the fit tight but also have minimal friction to enable rotation. This was reassuring given our device will need to be able to sustain a heavy amount of use. However, over repeated use, the string that was attached to the pulley gradually loosened and eventually popped clean off. Additionally, the range of applied force varied through trials, but the results of opening and closing were consistent amongst trials, something that will be necessary given our device will be used through human labor. The angle in which we applied force to activate our device did result in slight error. Though applying the force from a negative horizontal angle had no effect on the device (maybe marginal friction increases), applying a force from a positive horizontal angle resulted in the top gear popping out from its connection to the large gear, impeding the device’s ability to open and close as intended. 

<div style="display:grid; grid-template-columns:1fr 1fr; gap:12px; max-width:800px; margin:auto;">
  <img src="{{ '/assets/images/SLF/Use1.png' | relative_url }}" style="width:100%;">
  <img src="{{ '/assets/images/SLF/Use2.png' | relative_url }}" style="width:100%;">
</div>

- *Design Changes:*
  With these repeated use results, we will implement several changes to our future prototype. Primarily, we will adjust our pulley mechanism (likely through Fusion and subsequently printed in the RPL) to contain a contraption that ensures a tight, permanent connection between the string and the pulley. This will make sure that our prototype functions for all time. Additionally, we will need to implement a mechanism that limits the gear’s motion to solely rotational about our intended axis. The current presence of translational motion under specific force inputs is an issue over repeated use as there is a chance the piece falls out completely. The customer should not have to deal with these defects and thus, they will be solved in the next prototype. 

***4. Variable Radial Distances***
- *How it was tested:*
  We found real branches in the wild, similar in diameter to that of grape vines and executed multiple trials per diameter to analyze how our device makes contact with a variety of branch diameters. We also ran the device head along the length of each respective branch in each trial to document how the contact progressed throughout the device’s travel. Our thickest branch tested had a 1 inch diameter, the middle one had 0.5 inch diameter, and the thinnest one was 0.2 in diameter. 
- *What happened:*
  In the instance of the largest branch diameter, there was decent contact. In 8/10 trials, all teeth made contact with the branch, in 1/10 trials one tooth did not make contact and in 1/10 trials, 2 teeth did not make contact. In all trials, there was enough contact to hold the weight of the branch. However, the contact with each tooth onto the circumference of the tree branch only measured roughly 0.05” per tooth, which translates to 0.25” of coverage, whereas the branch itself is 3.14” of circumference. In the middle branch diameter, there was more consistent contact. In all 10 trials, each tooth sustained contact with the branch. This contact was shorter due to the nature of the branch and was roughly 0.02” per tooth. This translates to 0.1” of total circumference coverage out of a total 1.5” of circumference. Finally, the thinnest branch retained full teeth contact 10/10 trials. This contact was more minimal at roughly 0.01” per tooth and 0.05” circumference coverage out of 0.6” of total circumference. All branches, regardless of radius, had the same poor contact with the device at 8%, 7%, and 8% contact respectively. This is a reflection of a fundamental issue with our design that will be resolved in the next iteration.

<div style="display:grid; grid-template-columns:1fr 1fr 1fr; gap:12px; max-width:900px; margin:auto;">
  <img src="{{ '/assets/images/SLF/Stick1.png' | relative_url }}" style="width:100%;">
  <img src="{{ '/assets/images/SLF/Stick2.png' | relative_url }}" style="width:100%;">
  <img src="{{ '/assets/images/SLF/Stick3.png' | relative_url }}" style="width:100%;">
</div>

- *Design Changes:*
  The biggest takeaway from these trials was a reflection on the difficulty of obtaining full circumference contact between the mechanism and the vine. We must edit our model to result in more circumference coverage on the vine. Ideally, every part of the surface is in contact with the scraper given the ability of the masses to exist on any part of the vine surface. There are several routes to go here. We can simply make material adjustments that are able to conform to the vine surface. We can also keep the rigidity but adjust the formation of the fins to result in a more overlapping structure that fully encloses the vine (eliminates the sharp point). Another easy way to increase contact would be simply to increase the number of fins, allowing for more contact with the vine’s circumference. Furthermore, from these tests we realized the necessity for the default stage of our scraper to be open, and for enclosement only to result from an applied force. Thus, we will seek to find a way for the input force to fight against some spring/elastic force that wants to return the device to an open-toothed equilibrium. 


### Success Criteria
*Context:* An effective radial iris mechanism that can reliably scrape spotted lanternfly egg masses from grape vines while remaining easy to operate and mechanically reliable. Ease of use and effective egg mass removal are the highest priorities.

*Itemized Criteria:* a lot of our criterion are high priority, 
- The mechanism should require low operating force; The force required to open and close the iris through the pulley system should remain within a comfortable hand-operated range of 5–15 N. Lower force is a high priority to ensure the device can be used repeatedly without fatigue. We are currently working on how to translate this pulley system to a more ergonomic handle design with perhaps a squeezing motion.
- The mechanism should effectively remove egg masses; When tested on simulated egg masses attached to a curved vine surface, the blades should successfully scrape the egg masses from the vine in the majority of trials without requiring excessive force. Higher removal success is a high priority.
- On the same note, the mechanism should maintain consistent blade contact with the vine; The iris blades should engage the vine radially and maintain even contact around the circumference to ensure effective scraping across different vine diameters. This is also a high priority.
- The mechanism should function reliably under repeated use: the gear system, pulley, and blades should withstand multiple opening and closing cycles with minimal slipping or mechanical failure. Fewer slips per cycle set is a medium priority, however reliable functionality overall is a high priority.
- The device should be simple to assemble and structurally stable; The housing, baseplate, and fasteners should keep the mechanism aligned during operation and prevent excessive movement or loosening of components. This is a medium priority.


*Exhibit-Day Demo:* One of the most relevant criteria for the Exhibit-Day is the repeated use of our mechanism. The purpose of Exhibit-Day is for the demonstration of our mechanical device. Our device will be shown numerous times, and thus needs to withstand the repeated use throughout the day. Additionally, another relevant criterion could be the egg mass removal effectivity, as a possibility for Exhibit-Day could be to set up another mock-egg mass/vine and show our device in action.  

### Steps Towards Final Prototype (Summarized)
The gear shell will be redesigned with a fully enclosed casing to prevent disengagement from the larger spur gear. This casing will constrain motion strictly to rotation about the intended axis, eliminating unwanted translational movement.
The current pulley-string interface failed under repeated use, so a more robust attachment method is required. The pulley will be redesigned (and RPL printed) to include a built-in retention feature. In parallel, the actuation method will evolve from a simple pull-string into a more ergonomic input system. A handle-based or squeeze mechanism will be explored to increase user comfort and maintain a constant force magnitude/direction. 
To improve performance across varying branch diameters and irregular geometries, a compliant element will be incorporated into the blade system to maintain consistent pressure even if the vine is not aligned. 
To prepare the device for real-world vineyard use, a telescoping handle will be added for extended reach and will provide a lightweight but rigid structure for portability. 


View our [Functional Prototype]({{ "/assets/SLF/ODP5.pdf" | relative_url }}) in PDF format.

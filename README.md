<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Abdulkadir Rangrej - IT & Network Specialist Portfolio</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f3f4f6; /* Light gray background */
        }
        .section-title {
            position: relative;
            display: inline-block;
            padding-bottom: 8px; /* Space for the underline */
        }
        .section-title::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 70%; /* Underline width */
            height: 3px;
            background-color: #6366f1; /* Indigo color for underline */
            border-radius: 9999px; /* Rounded ends for underline */
        }
        /* Custom scrollbar for better aesthetics */
        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #f1f1f1;
            border-radius: 10px;
        }
        ::-webkit-scrollbar-thumb {
            background: #888;
            border-radius: 10px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #555;
        }

        /* Modal specific styles */
        .modal {
            display: none; /* Hidden by default */
            position: fixed; /* Stay in place */
            z-index: 1000; /* Sit on top */
            left: 0;
            top: 0;
            width: 100%; /* Full width */
            height: 100%; /* Full height */
            overflow: auto; /* Enable scroll if needed */
            background-color: rgba(0,0,0,0.8); /* Black w/ opacity */
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            margin: auto;
            display: block;
            max-width: 90%;
            max-height: 90%;
            object-fit: contain; /* Ensure image fits within modal without cropping */
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            border-radius: 8px;
        }

        .close-button {
            position: absolute;
            top: 15px;
            right: 35px;
            color: #f1f1f1;
            font-size: 40px;
            font-weight: bold;
            transition: 0.3s;
            cursor: pointer;
        }

        .close-button:hover,
        .close-button:focus {
            color: #bbb;
            text-decoration: none;
            cursor: pointer;
        }
    </style>
</head>
<body class="text-gray-800">

    <!-- Header & Navigation -->
    <header class="bg-indigo-700 text-white shadow-lg py-4 sticky top-0 z-50">
        <nav class="container mx-auto px-6 flex justify-between items-center">
            <a href="#" class="text-2xl font-bold rounded-md px-2 py-1 hover:bg-indigo-600 transition duration-300">Abdulkadir R.</a>
            <div class="hidden md:flex space-x-6">
                <a href="#about" class="hover:text-indigo-200 transition duration-300">About</a>
                <a href="#skills" class="hover:text-indigo-200 transition duration-300">Skills</a>
                <a href="#experience" class="hover:text-indigo-200 transition duration-300">Experience</a>
                <a href="#projects" class="hover:text-indigo-200 transition duration-300">Projects</a>
                <a href="#certifications" class="hover:text-indigo-200 transition duration-300">Certifications</a>
                <a href="#contact" class="hover:text-indigo-200 transition duration-300">Contact</a>
            </div>
            <!-- Mobile Menu Button -->
            <button id="mobile-menu-button" class="md:hidden focus:outline-none">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
                </svg>
            </button>
        </nav>
        <!-- Mobile Menu Overlay -->
        <div id="mobile-menu" class="hidden md:hidden fixed inset-0 bg-indigo-700 bg-opacity-95 z-40">
            <div class="flex justify-end p-6">
                <button id="close-mobile-menu-button" class="text-white focus:outline-none">
                    <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
                    </svg>
                </button>
            </div>
            <nav class="flex flex-col items-center text-xl space-y-6 text-white">
                <a href="#about" class="py-2 hover:text-indigo-200 transition duration-300" onclick="hideMobileMenu()">About</a>
                <a href="#skills" class="py-2 hover:text-indigo-200 transition duration-300" onclick="hideMobileMenu()">Skills</a>
                <a href="#experience" class="py-2 hover:text-indigo-200 transition duration-300" onclick="hideMobileMenu()">Experience</a>
                <a href="#projects" class="py-2 hover:text-indigo-200 transition duration-300" onclick="hideMobileMenu()">Projects</a>
                <a href="#certifications" class="py-2 hover:text-indigo-200 transition duration-300" onclick="hideMobileMenu()">Certifications</a>
                <a href="#contact" class="py-2 hover:text-indigo-200 transition duration-300" onclick="hideMobileMenu()">Contact</a>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="hero" class="bg-gradient-to-r from-indigo-700 to-indigo-900 text-white py-20 md:py-32 flex items-center justify-center min-h-screen-75">
        <div class="container mx-auto px-6 text-center">
            <h1 class="text-4xl md:text-6xl font-bold mb-4 animate-fade-in-down">Abdulkadir Mohammed Hanif Rangrej</h1>
            <p class="text-xl md:text-2xl mb-8 animate-fade-in-up">Experienced IT Engineer & Network Support Specialist</p>
            <p class="max-w-2xl mx-auto text-lg md:text-xl leading-relaxed mb-10 animate-fade-in">
                Adept at troubleshooting network issues, optimizing system performance, and implementing disaster recovery strategies.
                Proven ability to enhance connectivity, reduce downtime, and improve IT security.
            </p>
            <div class="space-x-4">
                <a href="#projects" class="bg-white text-indigo-700 hover:bg-gray-200 transition duration-300 px-8 py-3 rounded-full shadow-lg font-semibold transform hover:scale-105 inline-block">View My Work</a>
                <a href="#contact" class="border border-white text-white hover:bg-white hover:text-indigo-700 transition duration-300 px-8 py-3 rounded-full shadow-lg font-semibold transform hover:scale-105 inline-block">Get in Touch</a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-16 md:py-24 bg-white">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 section-title mx-auto">About Me</h2>
            <div class="flex flex-col md:flex-row items-center md:space-x-12">
                <div class="md:w-1/3 mb-8 md:mb-0">
                    <!-- Placeholder for an image or an icon representing IT/Networking -->
                    <img src="https://placehold.co/400x400/6366f1/ffffff?text=IT+Specialist" alt="Abdulkadir Rangrej" class="rounded-full shadow-lg mx-auto md:mx-0 w-64 h-64 object-cover border-4 border-indigo-500">
                </div>
                <div class="md:w-2/3 text-lg leading-relaxed text-gray-700">
                    <p class="mb-4">
                        I am an experienced IT Engineer and Network Support Specialist with a robust background in managing complex IT infrastructures and enhancing cybersecurity protocols. My journey from a Senior Network Engineer to an IT Manager has equipped me with comprehensive skills in network configuration, system optimization, and strategic leadership.
                    </p>
                    <p class="mb-4">
                        I thrive on tackling challenging technical issues, ensuring seamless connectivity, and safeguarding digital assets. My expertise spans various network devices and firewall solutions, allowing me to design and implement resilient and secure IT environments. I am passionate about leveraging technology to drive efficiency and reliability.
                    </p>
                    <p>
                        My professional approach is rooted in proactive problem-solving, meticulous planning, and a commitment to continuous improvement. I am always seeking new opportunities to apply my skills and contribute to dynamic organizations focused on technological excellence.
                    </p>
                    <a href="https://linkedin.com/in/abdulkadir-rangrej" target="_blank" class="inline-flex items-center text-indigo-600 hover:text-indigo-800 mt-6 font-semibold">
                        Connect on LinkedIn
                        <svg class="ml-2 w-4 h-4" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10.293 15.707a1 1 0 010-1.414L14.586 10l-4.293-4.293a1 1 0 111.414-1.414l5 5a1 1 0 010 1.414l-5 5a1 1 0 01-1.414 0z" clip-rule="evenodd"></path><path fill-rule="evenodd" d="M4.293 15.707a1 1 0 010-1.414L8.586 10 4.293 5.707a1 1 0 011.414-1.414l5 5a1 1 0 010 1.414l-5 5a1 1 0 01-1.414 0z" clip-rule="evenodd"></path></svg>
                    </a>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="py-16 md:py-24 bg-gray-100">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 section-title mx-auto">Skills</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 text-center">
                <div class="bg-white p-6 rounded-lg shadow-md hover:shadow-xl transition duration-300 transform hover:-translate-y-1">
                    <h3 class="text-2xl font-semibold mb-4 text-indigo-600">Networking</h3>
                    <ul class="list-none space-y-2 text-gray-700">
                        <li>✅ Network Configuration & Troubleshooting</li>
                        <li>✅ Virtual Private Networks (VPNs)</li>
                        <li>✅ Cisco, HP, Aruba, DAX, Plexonics Switches</li>
                        <li>✅ Wireless Network & Access Points</li>
                    </ul>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-md hover:shadow-xl transition duration-300 transform hover:-translate-y-1">
                    <h3 class="text-2xl font-semibold mb-4 text-indigo-600">Cybersecurity</h3>
                    <ul class="list-none space-y-2 text-gray-700">
                        <li>✅ Firewalls & Intrusion Detection (Fortinet, Cyberoam)</li>
                        <li>✅ IT Security Protocols</li>
                        <li>✅ Risk Assessments</li>
                        <li>✅ Disaster Recovery Strategies</li>
                    </ul>
                </div>
                <div class="bg-white p-6 rounded-lg shadow-md hover:shadow-xl transition duration-300 transform hover:-translate-y-1">
                    <h3 class="text-2xl font-semibold mb-4 text-indigo-600">Systems & OS</h3>
                    <ul class="list-none space-y-2 text-gray-700">
                        <li>✅ Windows & Linux OS Management</li>
                        <li>✅ CCTV Surveillance & NAS/NVR Setup</li>
                        <li>✅ IT Infrastructure Management</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="py-16 md:py-24 bg-white">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 section-title mx-auto">Experience</h2>
            <div class="relative max-w-3xl mx-auto">
                <!-- Timeline Line -->
                <div class="absolute hidden md:block left-1/2 transform -translate-x-1/2 w-1 bg-indigo-200 h-full"></div>

                <!-- IT Manager -->
                <div class="mb-12 flex flex-col md:flex-row items-start md:justify-between relative">
                    <div class="md:w-5/12 text-right md:pr-8 mb-4 md:mb-0">
                        <div class="bg-indigo-500 text-white text-sm font-semibold px-4 py-1 rounded-full inline-block">July 2024 – Present</div>
                    </div>
                    <div class="hidden md:block absolute left-1/2 top-0 transform -translate-x-1/2 mt-1 -ml-1 h-4 w-4 rounded-full bg-indigo-700 border-2 border-white shadow-lg"></div>
                    <div class="bg-white rounded-lg shadow-lg p-6 md:w-5/12 w-full ml-auto md:ml-0 border-l-4 border-indigo-700 md:border-l-0 md:border-r-4">
                        <h3 class="text-2xl font-bold text-indigo-800">IT Manager</h3>
                        <p class="text-gray-600 mb-2">DC Jewelers – Indore</p>
                        <ul class="list-disc list-inside text-gray-700 space-y-1">
                            <li>Oversee IT infrastructure, ensuring optimal system performance and security.</li>
                            <li>Lead network planning and optimization, enhancing connectivity and reliability.</li>
                            <li>Develop and implement IT policies, improving efficiency across departments.</li>
                            <li>Manage team operations, providing technical guidance and leadership.</li>
                        </ul>
                    </div>
                </div>

                <!-- IT Support Engineer -->
                <div class="mb-12 flex flex-col md:flex-row items-start md:justify-between relative">
                    <div class="md:w-5/12 text-left md:pl-8 order-2 md:order-1 mt-4 md:mt-0">
                        <div class="bg-white rounded-lg shadow-lg p-6 w-full border-r-4 border-indigo-700 md:border-r-0 md:border-l-4">
                            <h3 class="text-2xl font-bold text-indigo-800">IT Support Engineer</h3>
                            <p class="text-gray-600 mb-2">RBZ Jewellers LTD., Ahmedabad</p>
                            <ul class="list-disc list-inside text-gray-700 space-y-1">
                                <li>Managed and secured company IT infrastructure & networks.</li>
                                <li>Reduced system downtime by 15% and implemented strong security protocols.</li>
                                <li>Led disaster recovery strategies, ensuring 99% system recovery in crises.</li>
                                <li>Conducted risk assessments, reducing IT threats by 30%.</li>
                            </ul>
                        </div>
                    </div>
                    <div class="md:w-5/12 text-right md:pr-8 mb-4 md:mb-0 order-1 md:order-2">
                        <div class="bg-indigo-500 text-white text-sm font-semibold px-4 py-1 rounded-full inline-block">March 2023 – June 2024</div>
                    </div>
                    <div class="hidden md:block absolute left-1/2 top-0 transform -translate-x-1/2 mt-1 -ml-1 h-4 w-4 rounded-full bg-indigo-700 border-2 border-white shadow-lg"></div>
                </div>

                <!-- Senior Network Engineer -->
                <div class="mb-12 flex flex-col md:flex-row items-start md:justify-between relative">
                    <div class="md:w-5/12 text-right md:pr-8 mb-4 md:mb-0">
                        <div class="bg-indigo-500 text-white text-sm font-semibold px-4 py-1 rounded-full inline-block">November 2020 – March 2023</div>
                    </div>
                    <div class="hidden md:block absolute left-1/2 top-0 transform -translate-x-1/2 mt-1 -ml-1 h-4 w-4 rounded-full bg-indigo-700 border-2 border-white shadow-lg"></div>
                    <div class="bg-white rounded-lg shadow-lg p-6 md:w-5/12 w-full ml-auto md:ml-0 border-l-4 border-indigo-700 md:border-l-0 md:border-r-4">
                        <h3 class="text-2xl font-bold text-indigo-800">Senior Network Engineer</h3>
                        <p class="text-gray-600 mb-2">Vardhan Insys, Ahmedabad</p>
                        <ul class="list-disc list-inside text-gray-700 space-y-1">
                            <li>Configured network switches (Cisco, HP, Aruba, DAX, Plexonics).</li>
                            <li>Implemented firewall configurations (Fortinet, Cyberoam).</li>
                            <li>Managed CCTV systems, NAS & NVR.</li>
                            <li>Maintained wireless network & access points.</li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects/Case Studies Section (Placeholder) -->
    <section id="projects" class="py-16 md:py-24 bg-gray-100">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 section-title mx-auto">Projects & Case Studies</h2>
            <p class="text-center text-gray-600 mb-10 max-w-3xl mx-auto">
                Here are some of the key initiatives and projects I've spearheaded, demonstrating my problem-solving skills and technical expertise in IT infrastructure and cybersecurity.
                **Remember to replace this content with your actual project details!**
            </p>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Project 1: Network Infrastructure Optimization -->
                <div class="bg-white rounded-lg shadow-md hover:shadow-xl transition duration-300 transform hover:-translate-y-1 overflow-hidden">
                    <img src="https://placehold.co/600x400/9b59b6/ffffff?text=Network+Diagram" alt="Network Infrastructure Project" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-indigo-700">Enterprise Network Optimization</h3>
                        <p class="text-gray-600 text-sm mb-4">Case Study | IT Support Engineer Role</p>
                        <p class="text-gray-700 mb-4">
                            Spearheaded an initiative to optimize the company's network infrastructure, addressing bottlenecks and improving overall system responsiveness.
                        </p>
                        <ul class="list-disc list-inside text-gray-700 text-sm mb-4">
                            <li>**Challenge:** Frequent network slowdowns impacting operational efficiency.</li>
                            <li>**Solution:** Reconfigured core switches, optimized routing protocols, and implemented QoS policies.</li>
                            <li>**Result:** Reduced system downtime by 15% and significantly improved network reliability.</li>
                        </ul>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-indigo-100 text-indigo-800 text-xs font-medium px-2.5 py-0.5 rounded-full">Cisco</span>
                            <span class="bg-indigo-100 text-indigo-800 text-xs font-medium px-2.5 py-0.5 rounded-full">HP Switches</span>
                            <span class="bg-indigo-100 text-indigo-800 text-xs font-medium px-2.5 py-0.5 rounded-full">Network Troubleshooting</span>
                        </div>
                        <a href="#" class="text-indigo-600 hover:text-indigo-800 font-semibold inline-flex items-center">
                            Learn More
                            <svg class="ml-1 w-4 h-4" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10.293 15.707a1 1 0 010-1.414L14.586 10l-4.293-4.293a1 1 0 111.414-1.414l5 5a1 1 0 010 1.414l-5 5a1 1 0 01-1.414 0z" clip-rule="evenodd"></path></svg>
                        </a>
                    </div>
                </div>

                <!-- Project 2: Robust Disaster Recovery Implementation -->
                <div class="bg-white rounded-lg shadow-md hover:shadow-xl transition duration-300 transform hover:-translate-y-1 overflow-hidden">
                    <img src="https://placehold.co/600x400/3498db/ffffff?text=DRP+Flowchart" alt="Disaster Recovery Project" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-indigo-700">Disaster Recovery Plan Development</h3>
                        <p class="text-gray-600 text-sm mb-4">Case Study | IT Support Engineer Role</p>
                        <p class="text-gray-700 mb-4">
                            Led the design and implementation of a comprehensive disaster recovery strategy to ensure business continuity during critical incidents.
                        </p>
                        <ul class="list-disc list-inside text-gray-700 text-sm mb-4">
                            <li>**Challenge:** Lack of a formalized and tested disaster recovery plan.</li>
                            <li>**Solution:** Developed RTO/RPO objectives, implemented data backup/replication, and conducted regular failover tests.</li>
                            <li>**Result:** Achieved 99% system recovery in crises, minimizing potential business disruption.</li>
                        </ul>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-indigo-100 text-indigo-800 text-xs font-medium px-2.5 py-0.5 rounded-full">DRP</span>
                            <span class="bg-indigo-100 text-indigo-800 text-xs font-medium px-2.5 py-0.5 rounded-full">Data Backup</span>
                            <span class="bg-indigo-100 text-indigo-800 text-xs font-medium px-2.5 py-0.5 rounded-full">System Recovery</span>
                        </div>
                        <a href="#" class="text-indigo-600 hover:text-indigo-800 font-semibold inline-flex items-center">
                            Learn More
                            <svg class="ml-1 w-4 h-4" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10.293 15.707a1 1 0 010-1.414L14.586 10l-4.293-4.293a1 1 0 111.414-1.414l5 5a1 1 0 010 1.414l-5 5a1 1 0 01-1.414 0z" clip-rule="evenodd"></path></svg>
                        </a>
                    </div>
                </div>

                <!-- Project 3: Firewall & Threat Reduction -->
                <div class="bg-white rounded-lg shadow-md hover:shadow-xl transition duration-300 transform hover:-translate-y-1 overflow-hidden">
                    <img src="https://placehold.co/600x400/e67e22/ffffff?text=Firewall+Config" alt="Firewall Configuration Project" class="w-full h-48 object-cover">
                    <div class="p-6">
                        <h3 class="text-2xl font-semibold mb-2 text-indigo-700">Enhanced Network Security with Firewall Configuration</h3>
                        <p class="text-gray-600 text-sm mb-4">Case Study | Senior Network Engineer Role</p>
                        <p class="text-gray-700 mb-4">
                            Implemented advanced firewall configurations and conducted regular risk assessments to bolster network defenses against cyber threats.
                        </p>
                        <ul class="list-disc list-inside text-gray-700 text-sm mb-4">
                            <li>**Challenge:** Increasing frequency of unauthorized access attempts and potential security breaches.</li>
                            <li>**Solution:** Configured Fortinet and Cyberoam firewalls, deployed intrusion detection systems, and refined access control policies.</li>
                            <li>**Result:** Reduced IT threats by 30% and significantly improved the overall security posture.</li>
                        </ul>
                        <div class="flex flex-wrap gap-2 mb-4">
                            <span class="bg-indigo-100 text-indigo-800 text-xs font-medium px-2.5 py-0.5 rounded-full">Fortinet</span>
                            <span class="bg-indigo-100 text-indigo-800 text-xs font-medium px-2.5 py-0.5 rounded-full">Cyberoam</span>
                            <span class="bg-indigo-100 text-indigo-800 text-xs font-medium px-2.5 py-0.5 rounded-full">Intrusion Detection</span>
                        </div>
                        <a href="#" class="text-indigo-600 hover:text-indigo-800 font-semibold inline-flex items-center">
                            Learn More
                            <svg class="ml-1 w-4 h-4" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M10.293 15.707a1 1 0 010-1.414L14.586 10l-4.293-4.293a1 1 0 111.414-1.414l5 5a1 1 0 010 1.414l-5 5a1 1 0 01-1.414 0z" clip-rule="evenodd"></path></svg>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Certifications Section -->
    <section id="certifications" class="py-16 md:py-24 bg-white">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl md:text-4xl font-bold text-center mb-12 section-title mx-auto">Certifications & Education</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-4xl mx-auto mb-12">
                <!-- Certifications List -->
                <div class="bg-gray-50 p-6 rounded-lg shadow-md border-l-4 border-indigo-600">
                    <h3 class="text-2xl font-semibold mb-4 text-indigo-800">Certifications</h3>
                    <ul class="list-disc list-inside text-gray-700 space-y-2">
                        <li>📜 EC-Council CODE RED (2022)</li>
                        <li>📜 Google Technical Support Fundamentals (2021)</li>
                        <li>📜 Fortinet NSE Certification (2020)</li>
                        <li>📜 AICTSD Member Registration (2020)</li>
                        <li>📜 Introduction to Critical Infrastructure Protection (2024)</li>
                        <li>📜 1 Million Prompters - AI Training (2024)</li>
                    </ul>
                </div>
                <!-- Education List -->
                <div class="bg-gray-50 p-6 rounded-lg shadow-md border-l-4 border-indigo-600">
                    <h3 class="text-2xl font-semibold mb-4 text-indigo-800">Education</h3>
                    <ul class="list-disc list-inside text-gray-700 space-y-2">
                        <li>High School Diploma – Computer Engineering | Jetking, Ahmedabad (2012)</li>
                        <li>High School Diploma – Commerce | Guru Krupa High School, Ahmedabad (2007)</li>
                        <li>SSC Certificate | Guru Krupa High School, Ahmedabad (2005)</li>
                    </ul>
                </div>
            </div>

            <!-- Certificate Gallery -->
            <h3 class="text-2xl font-bold text-center mb-8 section-title mx-auto" style="width: fit-content;">Certificate Gallery</h3>
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
                <!-- Certificate 1: Digital India -->
                <div class="bg-white rounded-lg shadow-md hover:shadow-xl transition duration-300 transform hover:-translate-y-1 cursor-pointer" onclick="openModal('uploaded:2869 (1240×1754).jpg-1c943dc8-b506-4502-80bc-50ba5fb15d71')">
                    <img src="uploaded:2869 (1240×1754).jpg-1c943dc8-b506-4502-80bc-50ba5fb15d71" alt="Digital India Certificate" class="w-full h-48 object-cover rounded-t-lg">
                    <div class="p-4 text-center">
                        <p class="font-semibold text-indigo-700">Digital India Participation</p>
                        <p class="text-sm text-gray-600">Sept 2021</p>
                    </div>
                </div>
                <!-- Certificate 2: Critical Infrastructure Protection -->
                <div class="bg-white rounded-lg shadow-md hover:shadow-xl transition duration-300 transform hover:-translate-y-1 cursor-pointer" onclick="openModal('uploaded:1000101427 (2362×1897).jpg-8638c925-83c1-4832-9421-f54fb4802d04')">
                    <img src="uploaded:1000101427 (2362×1897).jpg-8638c925-83c1-4832-9421-f54fb4802d04" alt="Critical Infrastructure Protection Certificate" class="w-full h-48 object-cover rounded-t-lg">
                    <div class="p-4 text-center">
                        <p class="font-semibold text-indigo-700">Critical Infrastructure Protection</p>
                        <p class="text-sm text-gray-600">Dec 2024</p>
                    </div>
                </div>
                <!-- Certificate 3: EC-Council CODE RED -->
                <div class="bg-white rounded-lg shadow-md hover:shadow-xl transition duration-300 transform hover:-translate-y-1 cursor-pointer" onclick="openModal('uploaded:7a23866e-2902-4e79-ab86-a7ff9d1457b7.png-f2b9c9ce-c74d-4375-a4af-dc4ce2e593ed')">
                    <img src="uploaded:7a23866e-2902-4e79-ab86-a7ff9d1457b7.png-f2b9c9ce-c74d-4375-a4af-dc4ce2e593ed" alt="EC-Council CODE RED Certificate" class="w-full h-48 object-cover rounded-t-lg">
                    <div class="p-4 text-center">
                        <p class="font-semibold text-indigo-700">EC-Council CODE RED</p>
                        <p class="text-sm text-gray-600">Mar 2022</p>
                    </div>
                </div>
                <!-- Certificate 4: 1 Million Prompters -->
                <div class="bg-white rounded-lg shadow-md hover:shadow-xl transition duration-300 transform hover:-translate-y-1 cursor-pointer" onclick="openModal('uploaded:abdulkadir-mohammad-hanif-rangrej-certificate_page-0001 (1).jpg-b8b672dc-a23f-409e-ac84-bf29a7ae5822')">
                    <img src="uploaded:abdulkadir-mohammad-hanif-rangrej-certificate_page-0001 (1).jpg-b8b672dc-a23f-409e-ac84-bf29a7ae5822" alt="1 Million Prompters Certificate" class="w-full h-48 object-cover rounded-t-lg">
                    <div class="p-4 text-center">
                        <p class="font-semibold text-indigo-700">1 Million Prompters - AI Training</p>
                        <p class="text-sm text-gray-600">2024</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- The Modal (for full-screen image view) -->
    <div id="imageModal" class="modal">
        <span class="close-button" onclick="closeModal()">&times;</span>
        <img class="modal-content" id="modalImage">
    </div>

    <!-- Contact Section -->
    <section id="contact" class="py-16 md:py-24 bg-gradient-to-r from-indigo-700 to-indigo-900 text-white">
        <div class="container mx-auto px-6 text-center">
            <h2 class="text-3xl md:text-4xl font-bold mb-12 section-title mx-auto text-white">Get in Touch</h2>
            <p class="text-xl mb-8 max-w-2xl mx-auto">
                I'm always open to discussing new projects, opportunities, or collaborations. Feel free to reach out!
            </p>
            <div class="flex flex-col items-center space-y-6">
                <a href="mailto:info@abdulkadirrangrej.info" class="bg-white text-indigo-700 hover:bg-gray-200 transition duration-300 px-8 py-4 rounded-full shadow-lg font-semibold transform hover:scale-105 inline-flex items-center group">
                    <svg class="w-6 h-6 mr-3 group-hover:animate-bounce" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"></path><path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"></path></svg>
                    info@abdulkadirrangrej.info
                </a>
                <a href="https://linkedin.com/in/abdulkadir-rangrej" target="_blank" class="bg-blue-600 text-white hover:bg-blue-700 transition duration-300 px-8 py-4 rounded-full shadow-lg font-semibold transform hover:scale-105 inline-flex items-center group">
                    <svg class="w-6 h-6 mr-3 group-hover:animate-pulse" fill="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M22.23 0H1.77C.79 0 0 .77 0 1.73v20.54C0 23.23.79 24 1.77 24h20.46c.98 0 1.77-.77 1.77-1.73V1.73c0-.96-.79-1.73-1.77-1.73zM7.16 20.45H3.5V8.19h3.66v12.26zM5.33 6.64c-1.16 0-2.09-.94-2.09-2.1S4.17 2.45 5.33 2.45c1.16 0 2.09.94 2.09 2.1S6.49 6.64 5.33 6.64zm15.11 13.81h-3.66V14.5c0-1.4-.5-2.35-1.75-2.35-1.25 0-2 .88-2.32 1.72-.12.31-.15.73-.15 1.15v6.52H9.28S9.33 8.52 9.33 8.19h3.66v1.54c.48-.75 1.4-1.81 3.3-1.81 2.39 0 4.19 1.57 4.19 4.96v7.57z"></path></svg>
                    LinkedIn Profile
                </a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-8 text-center">
        <div class="container mx-auto px-6">
            <p>&copy; <span id="current-year"></span> Abdulkadir Mohammed Hanif Rangrej. All rights reserved.</p>
            <p class="mt-2">Designed with Tailwind CSS.</p>
        </div>
    </footer>

    <script>
        // Set current year in footer
        document.getElementById('current-year').textContent = new Date().getFullYear();

        // Mobile menu toggle functionality
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');
        const closeMobileMenuButton = document.getElementById('close-mobile-menu-button');

        mobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.remove('hidden');
        });

        closeMobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.add('hidden');
        });

        // Hide mobile menu when a link is clicked
        function hideMobileMenu() {
            mobileMenu.classList.add('hidden');
        }

        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();

                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Modal functionality for certificates
        const imageModal = document.getElementById('imageModal');
        const modalImage = document.getElementById('modalImage');

        function openModal(imageSrc) {
            modalImage.src = imageSrc;
            imageModal.style.display = 'flex'; // Use flex to center the content
        }

        function closeModal() {
            imageModal.style.display = 'none';
        }

        // Close modal when clicking outside the image
        imageModal.addEventListener('click', (e) => {
            if (e.target === imageModal) {
                closeModal();
            }
        });
    </script>
</body>
</html>

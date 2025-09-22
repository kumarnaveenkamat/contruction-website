# Construction-website
 I create a modern construction company website with a clean, professional design that showcases services, projects, and company information.
import React, { useState } from 'react';
import { Button } from "/components/ui/button";

const ConstructionWebsite = () => {
  const [mobileMenuOpen, setMobileMenuOpen] = useState(false);

  return (
    <div className="min-h-screen bg-white text-black font-sans">
      {/* Header */}
      <header className="bg-white border-b border-gray-200 px-6 py-4">
        <div className="max-w-7xl mx-auto flex justify-between items-center">
          <div className="flex items-center">
            <h1 className="text-2xl font-bold">BUILDCORP</h1>
            <span className="ml-2 text-xs bg-black text-white px-2 py-1 rounded">CONSTRUCTION</span>
          </div>
          
          {/* Desktop Navigation */}
          <nav className="hidden md:flex space-x-8">
            <a href="#home" className="hover:text-gray-600 transition-colors">Home</a>
            <a href="#services" className="hover:text-gray-600 transition-colors">Services</a>
            <a href="#projects" className="hover:text-gray-600 transition-colors">Projects</a>
            <a href="#about" className="hover:text-gray-600 transition-colors">About</a>
            <a href="#contact" className="hover:text-gray-600 transition-colors">Contact</a>
          </nav>

          {/* Mobile Menu Button */}
          <button 
            className="md:hidden"
            onClick={() => setMobileMenuOpen(!mobileMenuOpen)}
          >
            <div className="w-6 h-0.5 bg-black mb-1.5"></div>
            <div className="w-6 h-0.5 bg-black mb-1.5"></div>
            <div className="w-6 h-0.5 bg-black"></div>
          </button>
        </div>

        {/* Mobile Navigation */}
        {mobileMenuOpen && (
          <div className="md:hidden mt-4 pb-4 border-b border-gray-200">
            <nav className="flex flex-col space-y-3 px-6">
              <a href="#home" className="py-2">Home</a>
              <a href="#services" className="py-2">Services</a>
              <a href="#projects" className="py-2">Projects</a>
              <a href="#about" className="py-2">About</a>
              <a href="#contact" className="py-2">Contact</a>
            </nav>
          </div>
        )}
      </header>

      {/* Hero Section */}
      <section id="home" className="py-20 bg-gray-50">
        <div className="max-w-7xl mx-auto px-6 text-center">
          <h2 className="text-4xl md:text-6xl font-bold mb-6">Building Excellence, Brick by Brick</h2>
          <p className="text-xl text-gray-600 mb-8 max-w-3xl mx-auto">
            Professional construction services with over 25 years of experience in commercial and residential projects
          </p>
          <div className="flex flex-col sm:flex-row gap |4 justify-center">
            <Button className="bg-black text-white hover:bg-gray-800 px-8 py-3">
              View Our Projects
            </Button>
            <Button variant="outline" className="border-black text-black hover:bg-gray-100 px-8 py-3">
              Get Estimate
            </Button>
          </div>
        </div>
      </section>

      {/* Services Section */}
      <section id="services" className="py-20 bg-white">
        <div className="max-w-7xl mx-auto px-6">
          <h2 className="text-3xl font-bold text-center mb-12">Our Services</h2>
          <div className="grid md:grid-cols-3 gap-8">
            {/* Service 1 */}
            <div className="bg-gray-50 p-6 rounded-lg">
              <div className="w-16 h-16 bg-black rounded-full flex items-center justify-center mb-4">
                <span className="text-white text-xl font-bold">01</span>
              </div>
              <h3 className="text-xl font-semibold mb-3">Commercial Construction</h3>
              <p className="text-gray-600">
                Office buildings, retail spaces, and commercial complexes built to the highest standards.
              </p>
            </div>

            {/* Service 2 */}
            <div className="bg-gray-50 p-6 rounded-lg">
              <div className="w-16 h-16 bg-black rounded-full flex items-center justify-center mb-4">
                <span className="text-white text-xl font-bold">02</span>
              </div>
              <h3 className="text-xl font-semibold mb-3">Residential Construction</h3>
              <p className="text-gray-600">
                Custom homes and residential developments with attention to detail and quality craftsmanship.
              </p>
            </div>

            {/* Service 3 */}
            <div className="bg-gray-50 p-6 rounded-lg">
              <div className="w-16 h-16 bg-black rounded-full flex items-center justify-center mb-4">
                <span className="text-white text-xl font-bold">03</span>
              </div>
              <h3 className="text-xl font-semibold mb-3">Renovation & Remodeling</h3>
              <p className="text-gray-600">
                Transforming existing spaces into modern, functional, and beautiful environments.
              </p>
            </div>
          </div>
        </div>
      </section>

      {/* Projects Section */}
      <section id="projects" className="py-20 bg-gray-50">
        <div className="max-w-7xl mx-auto px-6">
          <h2 className="text-3xl font-bold text-center mb-12">Featured Projects</h2>
          <div className="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
            {/* Project 1 */}
            <div className="bg-white rounded-lg overflow-hidden shadow-md">
              <img 
                src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Modern office building with glass facade and clean architectural lines&id=9eef8dca-b2c6-4e34-bf3d-9e697f0225b4" 
                alt="Modern office building with glass facade and clean architectural lines" 
                className="w-full h-48 object-cover"
              />
              <div className="p-6">
                <h3 className="text-xl font-semibold mb-2">City Center Office Complex</h3>
                <p className="text-gray-600 mb-4">15-story commercial building with sustainable design features</p>
                <Button variant="outline" className="w-full border-black text-black">
                  View Details
                </Button>
              </div>
            </div>

            {/* Project 2 */}
            <div className="bg-white rounded-lg overflow-hidden shadow-md">
              <img 
                src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Luxury residential home with modern architecture and large windows&id=9eef8dca-b2c6-4e34-bf3d-9e697f0225b4" 
                alt="Luxury residential home with modern architecture and large windows" 
                className="w-full h-48 object-cover"
              />
              <div className="p-6">
                <h3 className="text-xl font-semibold mb-2">Hillside Residence</h3>
                <p className="text-gray-600 mb-4">Custom luxury home with panoramic mountain views</p>
                <Button variant="outline" className="w-full border-black text-black">
                  View Details
                </Button>
              </div>
            </div>

            {/* Project 3 */}
            <div className="bg-white rounded-lg overflow-hidden shadow-md">
              <img 
                src="https://placeholder-image-service.onrender.com/image/400x300?prompt=Industrial warehouse facility with metal construction and loading docks&id=9eef8dca-b2c6-4e34-bf3d-9e697f0225b4" 
                alt="Industrial warehouse facility with metal construction and loading docks" 
                className="w-full h-48 object-cover"
              />
              <div className="p-6">
                <h3 className="text-xl font-semibold mb-2">Logistics Center</h3>
                <p className="text-gray-600 mb-4">100,000 sq ft distribution warehouse with advanced systems</p>
                <Button variant="outline" className="w-full border-black text-black">
                  View Details
                </Button>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* About Section */}
      <section id="about" className="py-20 bg-white">
        <div className="max-w-7xl mx-auto px-6">
          <div className="grid md:grid-cols-2 gap-12 items-center">
            <div>
              <h2 className="text-3xl font-bold mb-6">About BuildCorp Construction</h2>
              <p className="text-gray-600 mb-4">
                Founded in 1998, BuildCorp has established itself as a leader in the construction industry, 
                delivering exceptional projects across commercial, residential, and industrial sectors.
              </p>
              <p className="text-gray-600 mb-6">
                Our team of experienced professionals is committed to quality, safety, and innovation in every project we undertake. 
                We pride ourselves on building lasting relationships with our clients through transparency and excellence.
              </p>
              <div className="grid grid-cols-2 gap-6">
                <div>
                  <p className="text-4xl font-bold">25+</p>
                  <p className="text-gray-600">Years Experience</p>
                </div>
                <div>
                  <p className="text-4xl font-bold">500+</p>
                  <p className="text-gray-600">Projects Completed</p>
                </div>
              </div>
            </div>
            <div>
              <img 
                src="https://placeholder-image-service.onrender.com/image/500x400?prompt=Construction team wearing hard hats reviewing blueprints at building site&id=9eef8dca-b2c6-4e34-bf3d-9e697f0225b4" 
                alt="Construction team wearing hard hats reviewing blueprints at building site" 
                className="w-full rounded-lg shadow-md"
              />
            </div>
          </div>
        </div>
      </section>

      {/* Contact Section */}
      <section id="contact" className="py-20 bg-gray-50">
        <div className="max-w-4xl mx-auto px-6">
          <h2 className="text-3xl font-bold text-center mb-12">Get In Touch</h2>
          <div className="bg-white p-8 rounded-lg shadow-md">
            <div className="grid md:grid-cols-2 gap-8 mb-8">
              <div>
                <h3 className="text-xl font-semibold mb-4">Contact Information</h3>
                <p className="text-gray-600 mb-2">123 Construction Avenue</p>
                <p className="text-gray-600 mb-2">Buildersville, BC 12345</p>
                <p className="text-gray-600 mb-2">Phone: (555) 123-4567</p>
                <p className="text-gray-600">Email: info@buildcorp.com</p>
              </div>
              <div>
                <h3 className="text-xl font-semibold mb-4">Business Hours</h3>
                <p className="text-gray-600 mb-2">Monday - Friday: 8:00 AM - 6:00 PM</p>
                <p className="text-gray-600 mb-2">Saturday: 9:00 AM - 2:00 PM</p>
                <p className="text-gray-600">Sunday: Closed</p>
              </div>
            </div>
            <form className="space-y-4">
              <div className="grid md:grid-cols-2 gap-4">
                <div>
                  <label className="block text-sm font-medium mb-2">Name</label>
                  <input 
                    type="text" 
                    className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-black"
                    placeholder="Your name"
                  />
                </div>
                <div>
                  <label className="block text-sm font-medium mb-2">Email</label>
                  <input 
                    type="email" 
                    className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-black"
                    placeholder="Your email"
                  />
                </div>
              </div>
              <div>
                <label className="block text-sm font-medium mb-2">Message</label>
                <textarea 
                  className="w-full px-4 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-black"
                  rows={4}
                  placeholder="How can we help you?"
                ></textarea>
              </div>
              <Button className="w-full bg-black text-white hover:bg-gray-800 py-3">
                Send Message
              </Button>
            </form>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-black text-white py-12">
        <div className="max-w-7xl mx-auto px-6">
          <div className="grid md:grid-cols-4 gap-8">
            <div>
              <h3 className="text-xl font-bold mb-4">BUILDCORP</h3>
              <p className="text-gray-400">
                Excellence in construction since 1998. Quality, safety, and innovation in every project.
              </p>
            </div>
            <div>
              <h4 className="font-semibold mb-4">Services</h4>
              <ul className="space-y-2 text-gray-400">
                <li>Commercial Construction</li>
                <li>Residential Construction</li>
                <li>Renovation & Remodeling</li>
                <li>Project Management</li>
              </ul>
            </div>
            <div>
              <h4 className="font-semibold mb-4">Quick Links</h4>
              <ul className="space-y-2 text-gray-400">
                <li>About Us</li>
                <li>Our Projects</li>
                <li>Testimonials</li>
                <li>Careers</li>
              </ul>
            </div>
            <div>
              <h4 className="font-semibold mb-4">Connect</h4>
              <p className="text-gray-400 mb-4">Follow us on social media</p>
              <div className="flex space-x-4">
                <div className="w-8 h-8 bg-gray-700 rounded-full"></div>
                <div className="w-8 h-8 bg-gray-700 rounded-full"></div>
                <div className="w-8 h-8 bg-gray-700 rounded-full"></div>
                <div className="w-8 h-8 bg-gray-700 rounded-full"></div>
              </div>
            </div>
          </div>
          <div className="border-t border-gray-800 mt-8 pt-8 text-center text-gray-400">
            <p>© 2024 BuildCorp Construction. All rights reserved.</p>
          </div>
        </div>
      </footer>
    </div>
  );
};

export default ConstructionWebsite;

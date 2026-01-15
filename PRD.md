# Planning Guide

A professional landing page that connects settlement funders with individuals seeking advances on their settlement funds, helping fundees shop the market for optimal financing deals based on their timeline needs.

**Experience Qualities**:
1. **Professional** - Instills trust and credibility in financial services through polished design and clear information hierarchy
2. **Approachable** - Makes a complex financial process feel accessible and straightforward for people in stressful situations
3. **Efficient** - Guides users quickly to understanding the value proposition and taking action through a streamlined journey

**Complexity Level**: Content Showcase (information-focused) - This is a marketing landing page designed to educate visitors about the service, build trust through social proof, and drive conversions through a contact form.

## Essential Features

### Hero Section with Call-to-Action
- **Functionality**: Displays compelling headline, subheadline, and primary CTA button
- **Purpose**: Immediately communicate value proposition and drive users to contact form
- **Trigger**: Page load
- **Progression**: User lands on page → Reads headline → Clicks CTA → Scrolls to contact form
- **Success criteria**: Clear messaging visible above fold, CTA button prominently displayed and functional

### How It Works Process
- **Functionality**: Shows 3-4 step process with icons explaining the funding journey
- **Purpose**: Demystify the settlement advance process and set clear expectations
- **Trigger**: User scrolls to section
- **Progression**: User scrolls → Sees numbered steps → Understands process flow → Gains confidence
- **Success criteria**: Steps are visually distinct, easy to scan, and logically ordered

### Benefits Section
- **Functionality**: Highlights key advantages of using the platform (market shopping, best rates, timeline flexibility)
- **Purpose**: Reinforce value proposition with specific benefits
- **Trigger**: User scrolls to section
- **Progression**: User scrolls → Reads benefits → Understands competitive advantage → Builds trust
- **Success criteria**: 3-6 benefits clearly communicated with supporting icons/imagery

### Stats/Trust Indicators
- **Functionality**: Displays impressive numbers (settlements funded, average rates, customer satisfaction)
- **Purpose**: Build credibility through quantifiable achievements
- **Trigger**: User scrolls to section
- **Progression**: User scrolls → Sees statistics → Gains social proof → Increases trust
- **Success criteria**: Numbers are prominent, believable, and impactful

### Testimonials
- **Functionality**: Shows customer reviews with names and context
- **Purpose**: Provide social proof through real customer experiences
- **Trigger**: User scrolls to section
- **Progression**: User scrolls → Reads testimonials → Sees relatable stories → Feels reassured
- **Success criteria**: 3+ testimonials with authentic-feeling details

### Contact Form
- **Functionality**: Collects user information (name, email, phone, settlement details)
- **Purpose**: Generate qualified leads for the sales team
- **Trigger**: User clicks CTA or scrolls to form section
- **Progression**: User fills form → Submits → Sees confirmation → Receives follow-up
- **Success criteria**: Form validates input, shows clear success message, persists data using useKV

### Footer
- **Functionality**: Displays company info, links, and contact details
- **Purpose**: Provide additional context and legal/support information
- **Trigger**: User scrolls to bottom
- **Progression**: User scrolls → Finds additional info → Clicks links as needed
- **Success criteria**: All standard footer elements present and organized

## Edge Case Handling
- **Empty Form Submission**: Validate all required fields before submission, show inline error messages
- **Invalid Email/Phone**: Real-time validation with helpful error messages
- **Slow Network**: Show loading states on form submission
- **Mobile Layout**: Responsive design that works seamlessly on all screen sizes
- **Repeat Visitors**: Form persists previous inputs using useKV for convenience

## Design Direction
The design should evoke professionalism, trust, and financial stability while remaining warm and approachable. It should feel like a legitimate financial services platform that understands the stress and urgency of someone needing settlement funds. The aesthetic should balance corporate credibility with human empathy - serious enough to trust with money, friendly enough to feel supported.

## Color Selection
A sophisticated blue-green palette that evokes trust, stability, and financial growth.

- **Primary Color**: Deep teal/blue `oklch(0.42 0.12 250)` - Represents trust, professionalism, and financial services
- **Secondary Colors**: 
  - Lighter teal `oklch(0.65 0.08 200)` - Supporting color for secondary actions and accents
  - Soft off-white `oklch(0.98 0.005 250)` - Clean, professional background
- **Accent Color**: Warm coral/orange `oklch(0.68 0.18 35)` - Draws attention to CTAs and important elements, represents opportunity and energy
- **Foreground/Background Pairings**: 
  - Primary background (Off-white `oklch(0.98 0.005 250)`): Dark text `oklch(0.25 0.02 250)` - Ratio 13.5:1 ✓
  - Primary buttons (Deep teal `oklch(0.42 0.12 250)`): White text `oklch(0.98 0.005 250)` - Ratio 9.2:1 ✓
  - Accent (Coral `oklch(0.68 0.18 35)`): White text `oklch(1 0 0)` - Ratio 4.6:1 ✓
  - Card backgrounds (White `oklch(1 0 0)`): Dark text `oklch(0.25 0.02 250)` - Ratio 14.8:1 ✓

## Font Selection
Typography should convey modernity and professionalism while remaining highly readable for users who may be stressed or scanning quickly.

- **Typographic Hierarchy**:
  - H1 (Main Hero): Space Grotesk Bold / 48px (mobile: 32px) / tight tracking / -0.02em
  - H2 (Section Titles): Space Grotesk Semibold / 36px (mobile: 28px) / tight tracking / -0.01em  
  - H3 (Subsection): Space Grotesk Medium / 24px (mobile: 20px) / normal tracking
  - Body Text: Inter Regular / 16px / 1.6 line-height / normal tracking
  - Button Text: Space Grotesk Medium / 16px / normal tracking / uppercase
  - Captions/Small: Inter Regular / 14px / 1.5 line-height

## Animations
Animations should enhance the professional feel without being distracting - subtle, purposeful, and dignified. Use gentle fade-ins as sections scroll into view to create a sense of polish and guide attention. CTAs should have satisfying hover states with subtle scale/shadow changes. Form inputs should have smooth focus transitions. Page transitions between sections should feel fluid with scroll-based reveals using framer-motion.

## Component Selection
- **Components**: 
  - Hero: Custom section with shadcn Button for CTA
  - How It Works: Custom cards with shadcn Card components
  - Benefits: Grid of shadcn Card components with icons from Phosphor
  - Stats: Custom stat display with number animations
  - Testimonials: shadcn Card components in a responsive grid
  - Contact Form: shadcn Form with Input, Textarea, Select, and Button components
  - Footer: Custom footer component with links
  - Toast notifications: Sonner for form submission feedback

- **Customizations**: 
  - Hero section with background gradient pattern
  - Animated stat counters for the stats section
  - Custom card hover effects for benefits and testimonials

- **States**: 
  - Buttons: Clear hover states with subtle elevation and color shift
  - Form inputs: Focused state with ring color matching primary, error states in red
  - Cards: Subtle hover lift effect with shadow increase
  - Loading: Disabled button states during form submission

- **Icon Selection**: 
  - Phosphor icons throughout for consistency
  - Process steps: NumberCircleOne, NumberCircleTwo, NumberCircleThree, NumberCircleFour
  - Benefits: CheckCircle, Lightning, ShieldCheck, Users, Clock, TrendUp
  - Contact: Phone, Envelope, MapPin
  - Social: InstagramLogo, FacebookLogo, LinkedinLogo

- **Spacing**: 
  - Section padding: py-16 md:py-24 (64px to 96px)
  - Container max-width: max-w-7xl
  - Card padding: p-6 md:p-8
  - Gap between cards: gap-6 md:gap-8
  - Button padding: px-6 py-3

- **Mobile**: 
  - Single column layouts on mobile (< 768px)
  - Stacked hero content with image below text
  - Grid columns: 1 column mobile, 2-3 columns tablet/desktop
  - Touch-friendly button sizes (min 44px height)
  - Hamburger menu not needed (single-page scroll)
  - Reduced font sizes for headings on mobile

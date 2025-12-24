# CALL_FLOW05_Multilanguage-IVR-Call-Flow-Genesys-Cloud-Architect
This project demonstrates the implementation of a multilanguage IVR call flow in Genesys Cloud Architect using manual language selection. The flow allows callers to choose their preferred language (English or Hindi) and continues the call experience in the selected language across multiple menus and departments.

# Technologies Used

1.Genesys Cloud CX

2.Genesys Architect

3.Text-to-Speech (TTS)

4.User Prompts

5.Language Routing

6.Menu & Task Configuration


# Step-by-Step Implementation
# Step 1: Create TTS Prompts

Created Text-to-Speech (TTS) prompts in:

   English

   Hindi

# Prompts were designed for:
  Welcome greeting
  Language selection
  menu options (Tech Support & Sales)

# Step 2: Upload Prompts to Genesys

  Uploaded both English and Hindi prompts into:

  Admin → Prompt Management → User Prompts

  Each prompt includes:

  Language tag (ENG / HIN)

  Clear naming convention for easy identification

# Step 3: Language Configuration

  Defined supported languages in the flow:

  Primary Language: English (ENG)

  Secondary Language: Hindi (HIN)

# Step 4: Create Architect Inbound Call Flow

  Created a new Inbound Call Flow in Genesys Architect.

# Step 5: Initial Task – Welcome Greeting

  In the Initial Task, configured a welcome greeting:

  English prompt:
  “Thank you for calling AKR Bank Customer Happiness Center.”

  Hindi prompt:
  “AKR Bank Customer Happiness Center mein aapka swagat hai.”

  Both prompts are available before language selection.

# Step 6: Language Selection Menu

  Created a Menu block named Language Selection.

  Added multilingual prompts:

  English:
  Press 1 for English

  Hindi:
  Hindi ke liye 2 dabaiye

# Step 7: Language Selection Tasks

  Configured two menu options:

  Option 1 – English

  Option 2 – Hindi
  
  For each option:

  Added a Set Language action:

  Option 1 → Set Language = English (ENG)

  Option 2 → Set Language = Hindi (HIN)

  This ensures all subsequent prompts follow the selected language.

# Step 8: Department Selection Menu

  After language selection, created another Menu block for department routing.

  Menu options:

  Option 1: Technical Support

  Option 2: Sales Team

  Both menu prompts are configured in English and Hindi.

# Step 9: Department Tasks

  Created separate tasks for:

  Tech Support

  Sales

  Each task:

  Uses the selected language

  Plays prompts in English or Hindi automatically

  Can be extended for queue routing, agents, or skills
  
  Call Flow Summary
  
  Call received
  
  Welcome greeting (ENG + HIN)
  
  Language selection menu

  Language set using Set Language tool
  
  Department selection menu
  
  Call routed to Tech Support or Sales in selected language
  
# Key Highlights
  
  Manual language selection using menu-based routing
  
  Language persistence across entire call flow
  
  Multilingual prompts at every interaction point

# Scalable design for adding more languages (Use switch case instead of menu. So we can add multiple language)

# Future Enhancements

  Automatic language selection based on caller country/ANI
  
  Default language fallback logic
  
  Skill-based routing per language
  
  CRM integration for preferred language lookup

# Use Case

  This flow is suitable for:
  
  Banks
  
  Customer support centers
  
  Multilingual regions
  
  Enterprises serving diverse customer bases
  


  
Language selection

Menu options (Tech Support & Sales)

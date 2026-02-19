# Inline Assistant Mobile - Prototypes

Interactive HTML prototypes exploring how inline AI assistance could work on mobile devices.

## 🎯 Background

Desktop Comet browser has an inline assistant that appears when you select text, providing quick AI actions. These prototypes explore how to adapt this experience for mobile, where text selection is harder and screen space is limited.

## 📱 Prototypes

### [Reading Mode](reading-prototype.html)

**Concept:** Tap paragraph → instant assistance

- Click any paragraph to select entire text block
- Bottom sheet appears with quick actions:
  - ✓ Fact-check
  - 📖 Define
  - 📝 Summarize
  - 🌐 Translate
  - 💡 Explain
  - 🔗 Related info
- Custom prompt input for flexible queries
- Results would open in sidecar (not shown in prototype)

**Key insight:** Instead of fighting mobile text selection, make entire paragraphs/sentences tappable targets.

### [Writing Mode](writing-prototype.html)

**Concept:** Focus input → writing assistance appears

- Tap any text input field to activate assistance
- Bottom panel shows writing quick actions:
  - ✨ Improve writing (grammar & style)
  - 🔄 Rephrase
  - 💼 Make professional
  - ✂️ Make shorter
  - 📝 Expand
  - ➡️ Continue writing
- Custom prompt for specific requests
- Results would allow insertion back into field

**Key insight:** Similar to keyboard suggestions, but AI-powered and contextual.

## 🎨 Design Principles

1. **No custom text selection UI** - Too fiddly on mobile, use native or paragraph-level selection
2. **Bottom sheets** - Familiar mobile pattern, doesn't obscure content
3. **Quick actions first** - Most users want common operations, not custom prompts
4. **Sidecar for results** - Keep assistant compact, use existing full-screen sidecar for responses
5. **Visual continuity** - Show selected text in preview so context is clear

## 🚀 Try It

Open `index.html` in a browser (works best on mobile or with mobile device emulation):

```bash
# If you have Python installed
python3 -m http.server 8000

# Or just open the HTML files directly
open index.html
```

Then visit:
- http://localhost:8000/ - Index with links to both prototypes
- http://localhost:8000/reading-prototype.html
- http://localhost:8000/writing-prototype.html

## 💭 Open Questions

1. **Reading mode trigger:** Single tap paragraph vs long-press vs selection handles?
2. **Writing mode persistence:** Should assistance panel stay open while typing?
3. **Insert mechanism:** How to preview and insert AI suggestions back into text?
4. **Keyboard interaction:** How does native keyboard interact with assistance panel?
5. **Multi-paragraph selection:** Should we support selecting multiple paragraphs?

## 🔗 Related

- [Desktop inline assistant data analysis](../inline-assistant-data-analysis.md)
- [Indy fact-check bubbles prototype](https://www.example.com) (inspiration for reading mode)
- [Yandex mobile assistant](https://www.example.com) (similar writing mode implementation)

## 📝 Notes

- These are **UI/UX prototypes only** - no backend integration
- Animations and interactions are simplified
- Real implementation would need:
  - Smart paragraph detection
  - Keyboard height detection
  - Insert/replace text APIs
  - Backend query processing
  - Proper error handling
  - Loading states
  - A11y improvements

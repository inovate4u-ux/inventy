# inventy# Inventy – 3-Object Invention Challenge

This project connects Firebase, Stripe, and GitHub to power the **“Do You Want to Play a Game?” 3-Object Challenge** app.

## 🚀 Features
- **Free Trial** → 5 games free for new users  
- **Token Packs** → Buy tokens (1 token = 1 generation)  
- **Invention Pass (Monthly)** → Unlimited plays + premium features  
- Secure login required for all access  

## 🛠️ Tech Stack
- **Frontend**: React / Next.js (or your chosen client framework)  
- **Backend**: Firebase (Firestore, Auth, Cloud Functions)  
- **Payments**: Stripe (via `firestore-stripe-payments` extension)  
- **Hosting**: Firebase App Hosting (Node.js)  

## 📂 Firestore Structure
```plaintext
products/{productId}/prices/{priceId}   # Stripe-synced catalog
customers/{uid}                         # Stripe customer mapping
customers/{uid}/checkout_sessions       # Checkout session requests
customers/{uid}/subscriptions           # Subscription status
entitlements/{uid}                      # Token balance
trials/{uid}                            # Free trial marker

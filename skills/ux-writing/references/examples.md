# Content — Examples

Do/don’t pairs for common surfaces. Standards: [style-guide.md](style-guide.md).

## Buttons and labels

| Do | Don’t |
| -- | ----- |
| Save changes | Save Changes |
| Create project | Create a Project |
| Delete page | Delete! |
| Continue | Click here |

## Headings

| Do | Don’t |
| -- | ----- |
| Add members to your workspace | Adding Members To Your Workspace |
| Organize your to-do list | Want to Organize Your To-Do List? |
| Billing settings | Billing Settings. |

## Helper / field text

| Do | Don’t |
| -- | ----- |
| Use 8 or more characters with a mix of letters and numbers. | Password should be e.g. 8+ chars, etc. |
| We’ll send a confirmation to this address. | A confirmation will be sent. |

## Inclusive language

| Do | Don’t |
| -- | ----- |
| Set up your project in a few steps. | It’s easy to set up a new project. |
| Ask your admin to update their permissions. | Ask your admin to update his or her permissions. |
| About usage limits | Learn more |
| People who use a screen reader | The blind |

## Errors

| Do | Don’t |
| -- | ----- |
| We can’t save your changes. Check your connection and try again. | Oops! Something went wrong!!! |
| Upload failed | Upload fail |
| Enter a valid email address. | You entered a bad email. |
| We couldn’t load this page. Refresh or try again later. | The page couldn’t be loaded. |

**Title + body pattern:**

- **Title:** We can’t save your changes
- **Description:** Check your connection and try again.
- **Action:** Try again

## Success

| Do | Don’t |
| -- | ----- |
| Project created | Yay! Your awesome project is ready! |
| Invite sent | Invite sent!!! |

## Warnings

| Do | Don’t |
| -- | ----- |
| Delete this page? This can’t be undone. | Are you sure you want to delete????? |
| Your trial ends in 3 days. Add a payment method to keep access. | Uh-oh, tick tock on your trial 😅 |

## Empty states

| Do | Don’t |
| -- | ----- |
| **Title:** No projects yet · **Description:** Create a project to start collaborating. · **Action:** Create project | No data. |
| **Title:** No results · **Description:** Try a different search or clear filters. · **Action:** Clear filters | Nothing found. Have a piece of cake and try again. |

## Instructions referring to UI

| Do | Don’t |
| -- | ----- |
| Go to **Settings**, then **Members**. | Go to ‘Settings’ > Members. |
| Select **Create**, then choose **Board**. | Hit the Create button (easy!). |

## Dates and time (English illustrations only)

| Do | Don’t |
| -- | ----- |
| August 14, 2028 | August 14th, 2028 |
| 2020 to 2024 | 2020-2024 |
| every 2 weeks | fortnightly |
| 6:30 a.m. | 6:30am |
| Step 1 of 2 | Step 1/2 |

In product code, emit these via i18n/`Intl` — do not paste locale-locked strings for every user.

## Message → placement

| Need | Example copy | Placement pattern |
| ---- | ------------ | ----------------- |
| In-flow error | Title: Payment failed · Body: Update your card and try again. | Inline / section message (error) |
| Transient success | Project archived | Transient notice |
| Section warning | API tokens expire on Aug 14, 2028. | Inline / section message (warning) |
| System maintenance | Scheduled maintenance on Saturday. | Banner |
| No rows | No invoices yet. Create your first invoice. | Empty view |
| Destructive confirm | Delete workspace? This can’t be undone. | Modal / confirm dialog |
